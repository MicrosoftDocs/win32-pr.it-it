---
title: Uso delle icone
description: In questa sezione vengono forniti esempi di codice che illustrano come eseguire attività correlate alle icone.
ms.assetid: 5021d59a-7aae-4ddc-be66-9abdc75ad316
keywords:
- risorse, icone
- icone, creazione
- icone, visualizzazione
- icone, condivisione delle risorse
- creazione di icone
- visualizzazione di icone
- risorse icona Condivisione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e93f831e3411985ecfb9f841ade750acd4a61b
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/25/2021
ms.locfileid: "106333989"
---
# <a name="using-icons"></a><span data-ttu-id="17b80-110">Uso delle icone</span><span class="sxs-lookup"><span data-stu-id="17b80-110">Using Icons</span></span>

<span data-ttu-id="17b80-111">Negli argomenti seguenti viene descritto come eseguire determinate attività correlate alle icone:</span><span class="sxs-lookup"><span data-stu-id="17b80-111">The following topics describe how to perform certain tasks related to icons:</span></span>

-   [<span data-ttu-id="17b80-112">Creazione di un'icona</span><span class="sxs-lookup"><span data-stu-id="17b80-112">Creating an Icon</span></span>](#creating-an-icon)
-   [<span data-ttu-id="17b80-113">Visualizzazione di un'icona</span><span class="sxs-lookup"><span data-stu-id="17b80-113">Displaying an Icon</span></span>](#displaying-an-icon)
-   [<span data-ttu-id="17b80-114">Risorse icona Condivisione</span><span class="sxs-lookup"><span data-stu-id="17b80-114">Sharing Icon Resources</span></span>](#sharing-icon-resources)

## <a name="creating-an-icon"></a><span data-ttu-id="17b80-115">Creazione di un'icona</span><span class="sxs-lookup"><span data-stu-id="17b80-115">Creating an Icon</span></span>

<span data-ttu-id="17b80-116">Per usare un'icona, l'applicazione deve ottenere un handle per l'icona.</span><span class="sxs-lookup"><span data-stu-id="17b80-116">To use an icon, your application must get a handle to the icon.</span></span> <span data-ttu-id="17b80-117">Nell'esempio seguente viene illustrato come creare due handle di icona diversi, uno per l'icona della domanda standard e uno per un'icona personalizzata inclusa come risorsa nel file di definizione delle risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="17b80-117">The following example shows how to create two different icon handles: one for the standard question icon and one for a custom icon included as a resource in the application's resource-definition file.</span></span>


```
HICON hIcon1;   // icon handle 
HICON hIcon2;   // icon handle 
 
// Create a standard question icon. 
 
hIcon1 = LoadIcon(NULL, IDI_QUESTION); 
 
// Create a custom icon based on a resource. 
 
hIcon2 = LoadIcon(hinst, MAKEINTRESOURCE(460)); 
 
// Create a custom icon at run time.
 
```



<span data-ttu-id="17b80-118">Un'applicazione deve implementare icone personalizzate come risorse e usare la funzione [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) o [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) , anziché creare le icone in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="17b80-118">An application should implement custom icons as resources and should use the [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) or [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) function, rather than create the icons at run-time.</span></span> <span data-ttu-id="17b80-119">Questo approccio evita la dipendenza dei dispositivi, semplifica la localizzazione e consente alle applicazioni di condividere le bitmap dell'icona.</span><span class="sxs-lookup"><span data-stu-id="17b80-119">This approach avoids device dependence, simplifies localization, and enables applications to share icon bitmaps.</span></span> <span data-ttu-id="17b80-120">Tuttavia, nell'esempio seguente viene usato [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) per creare un'icona personalizzata in fase di esecuzione, in base alle maschere di bit bitmap; è incluso per illustrare il modo in cui il sistema interpreta le maschere di bit Bitmap icona.</span><span class="sxs-lookup"><span data-stu-id="17b80-120">However, the following example uses [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) to create a custom icon at run-time, based on bitmap bitmasks; it is included to illustrate how the system interprets icon bitmap bitmasks.</span></span>


```
HICON hIcon3;      // icon handle 
 
// Yang icon AND bitmask 
 
BYTE ANDmaskIcon[] = {0xFF, 0xFF, 0xFF, 0xFF,   // line 1 
                      0xFF, 0xFF, 0xC3, 0xFF,   // line 2 
                      0xFF, 0xFF, 0x00, 0xFF,   // line 3 
                      0xFF, 0xFE, 0x00, 0x7F,   // line 4 
 
                      0xFF, 0xFC, 0x00, 0x1F,   // line 5 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 6 
                      0xFF, 0xF8, 0x00, 0x0F,   // line 7 
                      0xFF, 0xF0, 0x00, 0x07,   // line 8 
 
                      0xFF, 0xF0, 0x00, 0x03,   // line 9 
                      0xFF, 0xE0, 0x00, 0x03,   // line 10 
                      0xFF, 0xE0, 0x00, 0x01,   // line 11 
                      0xFF, 0xE0, 0x00, 0x01,   // line 12 
 
                      0xFF, 0xF0, 0x00, 0x01,   // line 13 
                      0xFF, 0xF0, 0x00, 0x00,   // line 14 
                      0xFF, 0xF8, 0x00, 0x00,   // line 15 
                      0xFF, 0xFC, 0x00, 0x00,   // line 16 
 
                      0xFF, 0xFF, 0x00, 0x00,   // line 17 
                      0xFF, 0xFF, 0x80, 0x00,   // line 18 
                      0xFF, 0xFF, 0xE0, 0x00,   // line 19 
                      0xFF, 0xFF, 0xE0, 0x01,   // line 20 
 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 21 
                      0xFF, 0xFF, 0xF0, 0x01,   // line 22 
                      0xFF, 0xFF, 0xF0, 0x03,   // line 23 
                      0xFF, 0xFF, 0xE0, 0x03,   // line 24 
 
                      0xFF, 0xFF, 0xE0, 0x07,   // line 25 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 26 
                      0xFF, 0xFF, 0xC0, 0x0F,   // line 27 
                      0xFF, 0xFF, 0x80, 0x1F,   // line 28 
 
                      0xFF, 0xFF, 0x00, 0x7F,   // line 29 
                      0xFF, 0xFC, 0x00, 0xFF,   // line 30 
                      0xFF, 0xF8, 0x03, 0xFF,   // line 31 
                      0xFF, 0xFC, 0x3F, 0xFF};  // line 32 
 
// Yang icon XOR bitmask 
 
BYTE XORmaskIcon[] = {0x00, 0x00, 0x00, 0x00,   // line 1 
                      0x00, 0x00, 0x00, 0x00,   // line 2 
                      0x00, 0x00, 0x00, 0x00,   // line 3 
                      0x00, 0x00, 0x00, 0x00,   // line 4 
 
                      0x00, 0x00, 0x00, 0x00,   // line 5 
                      0x00, 0x00, 0x00, 0x00,   // line 6 
                      0x00, 0x00, 0x00, 0x00,   // line 7 
                      0x00, 0x00, 0x38, 0x00,   // line 8 
 
                      0x00, 0x00, 0x7C, 0x00,   // line 9 
                      0x00, 0x00, 0x7C, 0x00,   // line 10 
                      0x00, 0x00, 0x7C, 0x00,   // line 11 
                      0x00, 0x00, 0x38, 0x00,   // line 12 
 
                      0x00, 0x00, 0x00, 0x00,   // line 13 
                      0x00, 0x00, 0x00, 0x00,   // line 14 
                      0x00, 0x00, 0x00, 0x00,   // line 15 
                      0x00, 0x00, 0x00, 0x00,   // line 16 
 
                      0x00, 0x00, 0x00, 0x00,   // line 17 
                      0x00, 0x00, 0x00, 0x00,   // line 18 
                      0x00, 0x00, 0x00, 0x00,   // line 19 
                      0x00, 0x00, 0x00, 0x00,   // line 20 
 
                      0x00, 0x00, 0x00, 0x00,   // line 21 
                      0x00, 0x00, 0x00, 0x00,   // line 22 
                      0x00, 0x00, 0x00, 0x00,   // line 23 
                      0x00, 0x00, 0x00, 0x00,   // line 24 
 
                      0x00, 0x00, 0x00, 0x00,   // line 25 
                      0x00, 0x00, 0x00, 0x00,   // line 26 
                      0x00, 0x00, 0x00, 0x00,   // line 27 
                      0x00, 0x00, 0x00, 0x00,   // line 28 
 
                      0x00, 0x00, 0x00, 0x00,   // line 29 
                      0x00, 0x00, 0x00, 0x00,   // line 30 
                      0x00, 0x00, 0x00, 0x00,   // line 31 
                      0x00, 0x00, 0x00, 0x00};  // line 32 
 
hIcon3 = CreateIcon(hinst,    // application instance  
             32,              // icon width 
             32,              // icon height 
             1,               // number of XOR planes 
             1,               // number of bits per pixel 
             ANDmaskIcon,     // AND bitmask  
             XORmaskIcon);    // XOR bitmask 
              
```



<span data-ttu-id="17b80-121">Per creare l'icona, [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) applica la seguente tabella di verità alle maschere di maschera and e XOR.</span><span class="sxs-lookup"><span data-stu-id="17b80-121">To create the icon, [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) applies the following truth table to the AND and XOR bitmasks.</span></span>



| <span data-ttu-id="17b80-122">E maschera di maschera</span><span class="sxs-lookup"><span data-stu-id="17b80-122">AND bitmask</span></span> | <span data-ttu-id="17b80-123">Maschera di maschera XOR</span><span class="sxs-lookup"><span data-stu-id="17b80-123">XOR bitmask</span></span> | <span data-ttu-id="17b80-124">Visualizza</span><span class="sxs-lookup"><span data-stu-id="17b80-124">Display</span></span>        |
|-------------|-------------|----------------|
| <span data-ttu-id="17b80-125">0</span><span class="sxs-lookup"><span data-stu-id="17b80-125">0</span></span>           | <span data-ttu-id="17b80-126">0</span><span class="sxs-lookup"><span data-stu-id="17b80-126">0</span></span>           | <span data-ttu-id="17b80-127">Black</span><span class="sxs-lookup"><span data-stu-id="17b80-127">Black</span></span>          |
| <span data-ttu-id="17b80-128">0</span><span class="sxs-lookup"><span data-stu-id="17b80-128">0</span></span>           | <span data-ttu-id="17b80-129">1</span><span class="sxs-lookup"><span data-stu-id="17b80-129">1</span></span>           | <span data-ttu-id="17b80-130">White</span><span class="sxs-lookup"><span data-stu-id="17b80-130">White</span></span>          |
| <span data-ttu-id="17b80-131">1</span><span class="sxs-lookup"><span data-stu-id="17b80-131">1</span></span>           | <span data-ttu-id="17b80-132">0</span><span class="sxs-lookup"><span data-stu-id="17b80-132">0</span></span>           | <span data-ttu-id="17b80-133">Screen</span><span class="sxs-lookup"><span data-stu-id="17b80-133">Screen</span></span>         |
| <span data-ttu-id="17b80-134">1</span><span class="sxs-lookup"><span data-stu-id="17b80-134">1</span></span>           | <span data-ttu-id="17b80-135">1</span><span class="sxs-lookup"><span data-stu-id="17b80-135">1</span></span>           | <span data-ttu-id="17b80-136">Inverti schermata</span><span class="sxs-lookup"><span data-stu-id="17b80-136">Reverse screen</span></span> |



 

<span data-ttu-id="17b80-137">Prima di chiudere, l'applicazione deve usare [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) per eliminare qualsiasi icona creata usando [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect).</span><span class="sxs-lookup"><span data-stu-id="17b80-137">Before closing, your application must use [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) to destroy any icon it created by using [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect).</span></span> <span data-ttu-id="17b80-138">Non è necessario eliminare le icone create da altre funzioni.</span><span class="sxs-lookup"><span data-stu-id="17b80-138">It is not necessary to destroy icons created by other functions.</span></span>

## <a name="displaying-an-icon"></a><span data-ttu-id="17b80-139">Visualizzazione di un'icona</span><span class="sxs-lookup"><span data-stu-id="17b80-139">Displaying an Icon</span></span>

<span data-ttu-id="17b80-140">L'applicazione può caricare e creare icone da visualizzare nell'area client dell'applicazione o nelle finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="17b80-140">Your application can load and create icons to display in the application's client area or child windows.</span></span> <span data-ttu-id="17b80-141">Nell'esempio seguente viene illustrato come creare un'icona nell'area client della finestra il cui contesto di dispositivo (DC) viene identificato dal parametro *HDC* .</span><span class="sxs-lookup"><span data-stu-id="17b80-141">The following example demonstrates how to draw an icon in the client area of the window whose device context (DC) is identified by the *hdc* parameter.</span></span>


```
HICON hIcon1;   // icon handle  
HDC hdc;        // handle to display context 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



<span data-ttu-id="17b80-142">Il sistema visualizza automaticamente le icone della classe per una finestra.</span><span class="sxs-lookup"><span data-stu-id="17b80-142">The system automatically displays the class icon(s) for a window.</span></span> <span data-ttu-id="17b80-143">L'applicazione può assegnare icone della classe durante la registrazione di una classe di finestra.</span><span class="sxs-lookup"><span data-stu-id="17b80-143">Your application can assign class icons while registering a window class.</span></span> <span data-ttu-id="17b80-144">L'applicazione può sostituire un'icona di classe usando la funzione [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) .</span><span class="sxs-lookup"><span data-stu-id="17b80-144">Your application can replace a class icon by using the [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) function.</span></span> <span data-ttu-id="17b80-145">Questa funzione modifica le impostazioni predefinite della finestra per tutte le finestre di una determinata classe.</span><span class="sxs-lookup"><span data-stu-id="17b80-145">This function changes the default window settings for all windows of a given class.</span></span> <span data-ttu-id="17b80-146">Nell'esempio seguente viene sostituita un'icona di classe con l'icona il cui identificatore di risorsa è 480.</span><span class="sxs-lookup"><span data-stu-id="17b80-146">The following example replaces a class icon with the icon whose resource identifier is 480.</span></span>


```
HINSTANCE hinst;            // handle to current instance 
HWND hwnd;                  // main window handle  
 
// Change the icon for hwnd's window class. 
 
SetClassLong(hwnd,          // window handle 
    GCL_HICON,              // changes icon 
    (LONG) LoadIcon(hinst, MAKEINTRESOURCE(480))
   ); 
```



<span data-ttu-id="17b80-147">Per ulteriori informazioni sulle classi della finestra, vedere [classi di finestra](/windows/desktop/winmsg/window-classes).</span><span class="sxs-lookup"><span data-stu-id="17b80-147">For more information about window classes, see [Window Classes](/windows/desktop/winmsg/window-classes).</span></span>

## <a name="sharing-icon-resources"></a><span data-ttu-id="17b80-148">Risorse icona Condivisione</span><span class="sxs-lookup"><span data-stu-id="17b80-148">Sharing Icon Resources</span></span>

<span data-ttu-id="17b80-149">Il codice seguente usa le funzioni [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon)e [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex)e alcune delle funzioni delle risorse per creare un handle di icona basato sui dati delle icone di un altro file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="17b80-149">The following code uses the functions [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon), and [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex), and several of the resource functions, to create an icon handle based on icon data from another executable file.</span></span> <span data-ttu-id="17b80-150">Quindi Visualizza l'icona in una finestra.</span><span class="sxs-lookup"><span data-stu-id="17b80-150">Then, it displays the icon in a window.</span></span>

<span data-ttu-id="17b80-151">**Avviso di sicurezza:** L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta.</span><span class="sxs-lookup"><span data-stu-id="17b80-151">**Security Warning:** Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="17b80-152">Per informazioni su come caricare correttamente le dll con versioni diverse di Windows, vedere la documentazione di **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="17b80-152">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```
HICON hIcon1;       // icon handle 
HINSTANCE hExe;     // handle to loaded .EXE file 
HRSRC hResource;    // handle to FindResource  
HRSRC hMem;         // handle to LoadResource 
BYTE *lpResource;   // pointer to resource data  
int nID;            // ID of resource that best fits current screen 
 
HDC hdc;        // handle to display context 
 
// Load the file from which to copy the icon. 
// Note: LoadLibrary should have a fully explicit path.
//
hExe = LoadLibrary("myapp.exe");
if (hExe == NULL)
{
    //Error loading module -- fail as securely as possible
    return;
}
 
 
// Find the icon directory whose identifier is 440. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(440), 
    RT_GROUP_ICON); 
 
// Load and lock the icon directory. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Get the identifier of the icon that is most appropriate 
// for the video display. 
 
nID = LookupIconIdFromDirectoryEx((PBYTE) lpResource, TRUE, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Find the bits for the nID icon. 
 
hResource = FindResource(hExe, 
    MAKEINTRESOURCE(nID), 
    MAKEINTRESOURCE(RT_ICON)); 
 
// Load and lock the icon. 
 
hMem = LoadResource(hExe, hResource); 
 
lpResource = LockResource(hMem); 
 
// Create a handle to the icon. 
 
hIcon1 = CreateIconFromResourceEx((PBYTE) lpResource, 
    SizeofResource(hExe, hResource), TRUE, 0x00030000, 
    CXICON, CYICON, LR_DEFAULTCOLOR); 
 
// Draw the icon in the client area. 
 
DrawIcon(hdc, 10, 20, hIcon1); 
```



 

 
