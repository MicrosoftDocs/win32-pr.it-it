---
description: Questo programma controlla la presenza e la configurazione dei componenti MicrosoftTablet PC e Touch Technology core.
ms.assetid: 0b379dc9-a86f-40c0-9403-d9c9091ca8c3
title: Esempio di informazioni sulla piattaforma Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d815f21233b1edcc90d456df68b3736c170a5fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317902"
---
# <a name="tablet-pc-platform-info-sample"></a><span data-ttu-id="30ebc-103">Esempio di informazioni sulla piattaforma Tablet PC</span><span class="sxs-lookup"><span data-stu-id="30ebc-103">Tablet PC Platform Info Sample</span></span>

<span data-ttu-id="30ebc-104">Questo programma controlla la presenza e la configurazione dei componenti MicrosoftTablet PC e Touch Technology core.</span><span class="sxs-lookup"><span data-stu-id="30ebc-104">This program checks the presence and configuration of the MicrosoftTablet PC and Touch Technology core components.</span></span> <span data-ttu-id="30ebc-105">Determina se i componenti tablet PC sono abilitati nel sistema operativo, elencando i nomi e le informazioni sulla versione per i controlli di base e il riconoscimento vocale e della grafia predefiniti.</span><span class="sxs-lookup"><span data-stu-id="30ebc-105">It determines whether Tablet PC components are enabled in the operating system, listing names and version information for core controls and the default handwriting and speech recognizer.</span></span>

<span data-ttu-id="30ebc-106">L'applicazione usa l'API Windows GetSystemMetrics, passando in SM \_ TABLETPC, per determinare se l'applicazione è in esecuzione in un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="30ebc-106">The application uses the GetSystemMetrics Windows API, passing in SM\_TABLETPC, to determine whether the application running on a Tablet PC.</span></span> <span data-ttu-id="30ebc-107">Il \_ TABLETPC SM è definito in winuser. h.</span><span class="sxs-lookup"><span data-stu-id="30ebc-107">SM\_TABLETPC is defined in WinUser.h.</span></span>

<span data-ttu-id="30ebc-108">Di particolare interesse è il modo in cui l'applicazione usa la raccolta Recognizers per fornire informazioni sul riconoscimento predefinito.</span><span class="sxs-lookup"><span data-stu-id="30ebc-108">Of particular interest is the way the application uses the Recognizers collection to provide information about the default recognizer.</span></span> <span data-ttu-id="30ebc-109">Prima di provare a usare la raccolta Recognizers e l'oggetto Recognizer, l'applicazione verifica la corretta creazione.</span><span class="sxs-lookup"><span data-stu-id="30ebc-109">Before attempting to use the Recognizers collection and Recognizer object, the application tests for their successful creation.</span></span>

## <a name="components"></a><span data-ttu-id="30ebc-110">Componenti</span><span class="sxs-lookup"><span data-stu-id="30ebc-110">Components</span></span>

<span data-ttu-id="30ebc-111">Utilizzando il modulo merge ridistribuibile, è possibile che alcune parti dell'API della piattaforma Tablet PC siano installate in versioni non Tablet di vista e Windows XP Professional.</span><span class="sxs-lookup"><span data-stu-id="30ebc-111">Using the re-distributable merge module, certain parts of the Tablet PC Platform API may be installed on non-Tablet versions of Vista and Windows XP Professional .</span></span> <span data-ttu-id="30ebc-112">La chiamata GetSystemMetrics indica solo che è installato Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="30ebc-112">The GetSystemMetrics call only indicates that Windows XP Tablet PC Edition is installed.</span></span> <span data-ttu-id="30ebc-113">Un'applicazione deve sempre determinare se è disponibile un determinato componente.</span><span class="sxs-lookup"><span data-stu-id="30ebc-113">An application should always determine if a given component is available.</span></span> <span data-ttu-id="30ebc-114">Il modo corretto per determinare se un componente dell'API è installato consiste nel tentare di creare un'istanza di un oggetto o di un controllo e verificare che esista prima di provare a usarlo, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="30ebc-114">The proper way to determine if a component of the API is installed is to attempt to create an instance of an object or control and check that it exists before attempting to use it, as shown in the following example.</span></span>


```C++
IInkRecognizers* pIInkRecognizers = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkRecognizers,
                              NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IInkRecognizers, 
                              (void **)&pIInkRecognizers);
if (SUCCEEDED(hr)) 
{
  // use the component
} else
{
  // component unavailable
}
```



<span data-ttu-id="30ebc-115">L'applicazione individua i componenti vocali installati esaminando la chiave del registro di sistema appropriata:</span><span class="sxs-lookup"><span data-stu-id="30ebc-115">The application finds out about the installed speech components by looking in the appropriate registry key:</span></span>


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



<span data-ttu-id="30ebc-116">La chiave viene letta usando RegQueryValueExW.</span><span class="sxs-lookup"><span data-stu-id="30ebc-116">The key is read using RegQueryValueExW.</span></span>

<span data-ttu-id="30ebc-117">Infine, nell'esempio vengono individuati i controlli installati.</span><span class="sxs-lookup"><span data-stu-id="30ebc-117">Finally, the sample finds out which controls are installed.</span></span>


```C++
LPCOLESTR gc_wszProgId[NUM_CONTROLS] = {L"InkEd.InkEdit", L"msinkaut.InkOverlay"};
// ...
for (int i = 0, j = 0; i < NUM_CONTROLS; i++)
{
    // Get the component info
    CLSID clsid;
    if (SUCCEEDED(CLSIDFromProgID(gc_wszProgId[i], &clsid)) && GetComponentInfo(clsid, info) == TRUE)
    {
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][0], info.wchName);
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][1], info.wchVersion);
        j++;
    }
}
```



 

 



