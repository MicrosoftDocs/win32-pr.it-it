---
title: Riproduzione di risorse WAVE
description: Riproduzione di risorse WAVE
ms.assetid: e6129bf4-b83f-4c38-8b96-21aed66ba605
keywords:
- audio per la forma d'onda, risorse WAVE
- audio ausiliario, risorse di riproduzione WAVE
- riproduzione di risorse WAVE
- Funzione PlaySound, riproduzione di risorse WAVE
- sndPlaySound (funzione)
- Funzione PlaySound, confrontata con la funzione sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9678c18e09b12ee1e8d8215d0841cbdaba0ac9c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473067"
---
# <a name="playing-wave-resources"></a><span data-ttu-id="f921e-109">Riproduzione di risorse WAVE</span><span class="sxs-lookup"><span data-stu-id="f921e-109">Playing WAVE Resources</span></span>

<span data-ttu-id="f921e-110">È possibile usare la funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) per riprodurre un suono archiviato come risorsa.</span><span class="sxs-lookup"><span data-stu-id="f921e-110">You can use the [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function to play a sound that is stored as a resource.</span></span> <span data-ttu-id="f921e-111">Sebbene sia possibile anche usare la funzione [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) , **sndPlaySound** richiede di trovare, caricare, bloccare, sbloccare e liberare la risorsa; **PlaySound** consente di ottenere tutti questi risultati con una sola riga di codice.</span><span class="sxs-lookup"><span data-stu-id="f921e-111">Although this is also possible using the [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function, **sndPlaySound** requires that you find, load, lock, unlock, and free the resource; **PlaySound** achieves all of this with a single line of code.</span></span>

## <a name="playsound-example"></a><span data-ttu-id="f921e-112">Esempio di PlaySound</span><span class="sxs-lookup"><span data-stu-id="f921e-112">PlaySound Example</span></span>


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a><span data-ttu-id="f921e-113">Esempio di sndPlaySound</span><span class="sxs-lookup"><span data-stu-id="f921e-113">sndPlaySound Example</span></span>

<span data-ttu-id="f921e-114">Il \_ flag di memoria SND indica che il parametro *lpszSoundName* è un puntatore a un'immagine in memoria del file Wave.</span><span class="sxs-lookup"><span data-stu-id="f921e-114">The SND\_MEMORY flag indicates that the *lpszSoundName* parameter is a pointer to an in-memory image of the WAVE file.</span></span> <span data-ttu-id="f921e-115">Per includere un file WAVE come risorsa in un'applicazione, aggiungere la voce seguente allo script di risorsa dell'applicazione (. RC) file.</span><span class="sxs-lookup"><span data-stu-id="f921e-115">To include a WAVE file as a resource in an application, add the following entry to the application's resource script (.RC) file.</span></span>


```C++
soundName WAVE c:\sounds\bells.wav 
```



<span data-ttu-id="f921e-116">Il nome *soundName* è un segnaposto per il nome fornito per fare riferimento a questa risorsa Wave.</span><span class="sxs-lookup"><span data-stu-id="f921e-116">The name *soundName* is a placeholder for a name that you supply to refer to this WAVE resource.</span></span> <span data-ttu-id="f921e-117">Le risorse WAVE vengono caricate e accessibili in modo analogo alle altre risorse di Windows definite dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f921e-117">WAVE resources are loaded and accessed just like other application-defined Windows resources.</span></span> <span data-ttu-id="f921e-118">La funzione PlayResource nell'esempio seguente riproduce una risorsa WAVE specificata.</span><span class="sxs-lookup"><span data-stu-id="f921e-118">The PlayResource function in the following example plays a specified WAVE resource.</span></span>


```C++
BOOL PlayResource(LPSTR lpName) 
{ 
    BOOL bRtn; 
    LPSTR lpRes; 
    HANDLE hResInfo, hRes; 
 
    // Find the WAVE resource. 
 
    hResInfo = FindResource(hInst, lpName, "WAVE"); 
    if (hResInfo == NULL) 
        return FALSE; 
 
    // Load the WAVE resource. 
 
    hRes = LoadResource(hInst, hResInfo); 
    if (hRes == NULL) 
        return FALSE; 
 
    // Lock the WAVE resource and play it. 
 
    lpRes = LockResource(hRes); 
    if (lpRes != NULL) { 
        bRtn = sndPlaySound(lpRes, SND_MEMORY | SND_SYNC | 
            SND_NODEFAULT); 
        UnlockResource(hRes); 
    } 
    else 
        bRtn = 0; 
 
    // Free the WAVE resource and return success or failure. 
 
    FreeResource(hRes); 
    return bRtn; 
} 
```



<span data-ttu-id="f921e-119">Per riprodurre una risorsa WAVE usando questa funzione, passare alla funzione un puntatore a una stringa contenente il nome della risorsa, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="f921e-119">To play a WAVE resource by using this function, pass to the function a pointer to a string containing the name of the resource, as shown in the following example.</span></span>


```C++
PlayResource("soundName"); 
```



 

 