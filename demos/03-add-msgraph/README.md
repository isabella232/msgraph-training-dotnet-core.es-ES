# <a name="how-to-run-the-completed-project"></a><span data-ttu-id="083ee-101">Cómo ejecutar el proyecto completado</span><span class="sxs-lookup"><span data-stu-id="083ee-101">How to run the completed project</span></span>

## <a name="prerequisites"></a><span data-ttu-id="083ee-102">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="083ee-102">Prerequisites</span></span>

<span data-ttu-id="083ee-103">Para ejecutar el proyecto completado en esta carpeta, necesita lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="083ee-103">To run the completed project in this folder, you need the following:</span></span>

- <span data-ttu-id="083ee-104">[.Net Core SDK](https://dotnet.microsoft.com/download) instalado en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="083ee-104">The [.NET Core SDK](https://dotnet.microsoft.com/download) installed on your development machine.</span></span> <span data-ttu-id="083ee-105">(**Nota:** este tutorial se ha escrito con .net Core SDK versión 2.2.401.</span><span class="sxs-lookup"><span data-stu-id="083ee-105">(**Note:** This tutorial was written with .NET Core SDK version 2.2.401.</span></span> <span data-ttu-id="083ee-106">Los pasos de esta guía pueden funcionar con otras versiones, pero no se han probado.</span><span class="sxs-lookup"><span data-stu-id="083ee-106">The steps in this guide may work with other versions, but that has not been tested.)</span></span>
- <span data-ttu-id="083ee-107">Una cuenta profesional o educativa de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="083ee-107">A Microsoft work or school account.</span></span>

<span data-ttu-id="083ee-108">Si no tiene una cuenta de Microsoft, puede [suscribirse al programa de desarrolladores de office 365](https://developer.microsoft.com/office/dev-program) para obtener una suscripción gratuita a Office 365.</span><span class="sxs-lookup"><span data-stu-id="083ee-108">If you don't have a Microsoft account, you can [sign up for the Office 365 Developer Program](https://developer.microsoft.com/office/dev-program) to get a free Office 365 subscription.</span></span>

## <a name="register-a-web-application-with-the-azure-active-directory-admin-center"></a><span data-ttu-id="083ee-109">Registro de una aplicación web con el centro de administración de Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="083ee-109">Register a web application with the Azure Active Directory admin center</span></span>

1. <span data-ttu-id="083ee-110">Abra un explorador y vaya al [centro de administración de Azure Active Directory](https://aad.portal.azure.com) e inicie sesión con una **cuenta personal** (también conocida como: cuenta Microsoft) o una **cuenta profesional o educativa**.</span><span class="sxs-lookup"><span data-stu-id="083ee-110">Open a browser and navigate to the [Azure Active Directory admin center](https://aad.portal.azure.com) and login using a **personal account** (aka: Microsoft Account) or **Work or School Account**.</span></span>

1. <span data-ttu-id="083ee-111">Seleccione **Azure Active Directory** en el panel de navegación de la izquierda y, después, seleccione **registros de aplicaciones** en **administrar**.</span><span class="sxs-lookup"><span data-stu-id="083ee-111">Select **Azure Active Directory** in the left-hand navigation, then select **App registrations** under **Manage**.</span></span>

    ![<span data-ttu-id="083ee-112">Una captura de pantalla de los registros de la aplicación</span><span class="sxs-lookup"><span data-stu-id="083ee-112">A screenshot of the App registrations</span></span> ](/tutorial/images/aad-portal-app-registrations.png)

1. <span data-ttu-id="083ee-113">Seleccione **Nuevo registro**.</span><span class="sxs-lookup"><span data-stu-id="083ee-113">Select **New registration**.</span></span> <span data-ttu-id="083ee-114">En la página **Registrar una aplicación**, establezca los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="083ee-114">On the **Register an application** page, set the values as follows.</span></span>

    - <span data-ttu-id="083ee-115">Establezca **Nombre** como `.NET Core Graph Tutorial`.</span><span class="sxs-lookup"><span data-stu-id="083ee-115">Set **Name** to `.NET Core Graph Tutorial`.</span></span>
    - <span data-ttu-id="083ee-116">Establezca los **tipos de cuenta admitidos** **en las cuentas de cualquier directorio de la organización**.</span><span class="sxs-lookup"><span data-stu-id="083ee-116">Set **Supported account types** to **Accounts in any organizational directory**.</span></span>
    - <span data-ttu-id="083ee-117">Deje **URI de redireccionamiento** vacía.</span><span class="sxs-lookup"><span data-stu-id="083ee-117">Leave **Redirect URI** empty.</span></span>

    ![Captura de pantalla de la página registrar una aplicación](/tutorial/images/aad-register-an-app.png)

1. <span data-ttu-id="083ee-119">Seleccione **registrar**.</span><span class="sxs-lookup"><span data-stu-id="083ee-119">Select **Register**.</span></span> <span data-ttu-id="083ee-120">En la página **tutorial de .net Core Graph** , copie el valor del **identificador de la aplicación (cliente)** y guárdelo, lo necesitará en el paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="083ee-120">On the **.NET Core Graph Tutorial** page, copy the value of the **Application (client) ID** and save it, you will need it in the next step.</span></span>

    ![Captura de pantalla del identificador de la aplicación del nuevo registro de la aplicación](/tutorial/images/aad-application-id.png)

1. <span data-ttu-id="083ee-122">Seleccione el vínculo **Agregar un URI de redireccionamiento** .</span><span class="sxs-lookup"><span data-stu-id="083ee-122">Select the **Add a Redirect URI** link.</span></span> <span data-ttu-id="083ee-123">En la página **URI de redireccionamiento** , busque la sección **URI de redireccionamiento sugeridos para clientes públicos (móvil, escritorio)** .</span><span class="sxs-lookup"><span data-stu-id="083ee-123">On the **Redirect URIs** page, locate the **Suggested Redirect URIs for public clients (mobile, desktop)** section.</span></span> <span data-ttu-id="083ee-124">Seleccione el `https://login.microsoftonline.com/common/oauth2/nativeclient` URI.</span><span class="sxs-lookup"><span data-stu-id="083ee-124">Select the `https://login.microsoftonline.com/common/oauth2/nativeclient` URI.</span></span>

    ![Captura de pantalla de la página URI de redireccionamiento](/tutorial/images/aad-redirect-uris.png)

1. <span data-ttu-id="083ee-126">Busque la sección **tipo de cliente predeterminado** y cambie la opción **tratar aplicación como un cliente público** cambie a **sí**y, a continuación, elija **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="083ee-126">Locate the **Default client type** section and change the **Treat application as a public client** toggle to **Yes**, then choose **Save**.</span></span>

    ![Captura de pantalla de la sección tipo de cliente predeterminado](/tutorial/images/aad-default-client-type.png)

## <a name="configure-the-sample"></a><span data-ttu-id="083ee-128">Configuración del ejemplo</span><span class="sxs-lookup"><span data-stu-id="083ee-128">Configure the sample</span></span>

1. <span data-ttu-id="083ee-129">Cambie el nombre `appsettings.json.example` del archivo `appsettings.json`a.</span><span class="sxs-lookup"><span data-stu-id="083ee-129">Rename the `appsettings.json.example` file to `appsettings.json`.</span></span>
1. <span data-ttu-id="083ee-130">Edite `appsettings.json` el archivo y realice los cambios siguientes.</span><span class="sxs-lookup"><span data-stu-id="083ee-130">Edit the `appsettings.json` file and make the following changes.</span></span>
    1. <span data-ttu-id="083ee-131">Reemplace `YOUR_APP_ID_HERE` por el **identificador de aplicación** que obtuvo desde el portal de registro de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="083ee-131">Replace `YOUR_APP_ID_HERE` with the **Application Id** you got from the App Registration Portal.</span></span>

## <a name="build-and-run-the-sample"></a><span data-ttu-id="083ee-132">Compilar y ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="083ee-132">Build and run the sample</span></span>

<span data-ttu-id="083ee-133">En la interfaz de línea de comandos (CLI), navegue hasta el directorio del proyecto y ejecute los siguientes comandos.</span><span class="sxs-lookup"><span data-stu-id="083ee-133">In your command-line interface (CLI), navigate to the project directory and run the following commands.</span></span>

```Shell
dotnet restore
dotnet build
dotnet run
```