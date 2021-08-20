---
title: Riproduzione di risorse WAVE
description: Riproduzione di risorse WAVE
ms.assetid: e6129bf4-b83f-4c38-8b96-21aed66ba605
keywords:
- audio waveform, riproduzione di risorse WAVE
- audio ausiliario, riproduzione di risorse WAVE
- riproduzione di risorse WAVE
- Funzione PlaySound, riproduzione di risorse WAVE
- Funzione sndPlaySound
- Funzione PlaySound, confrontata con la funzione sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd256d3c4cf07d6d2f57ba9c4d85c54b9d0e599f9382a5b8d9d1f3a0ef4705ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136760"
---
# <a name="playing-wave-resources"></a>Riproduzione di risorse WAVE

È possibile usare la [**funzione PlaySound**](/previous-versions//dd743680(v=vs.85)) per riprodurre un suono archiviato come risorsa. Sebbene sia possibile usare anche la funzione [**sndPlaySound,**](/previous-versions//dd798676(v=vs.85)) **sndPlaySound** richiede di trovare, caricare, bloccare, sbloccare e liberare la risorsa. **PlaySound** consente di ottenere tutto questo con una singola riga di codice.

## <a name="playsound-example"></a>Esempio di PlaySound


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a>Esempio di sndPlaySound

Il flag MEMORY SND indica che il \_ *parametro lpszSoundName* è un puntatore a un'immagine in memoria del file WAVE. Per includere un file WAVE come risorsa in un'applicazione, aggiungere la voce seguente allo script di risorsa dell'applicazione (. RC).


```C++
soundName WAVE c:\sounds\bells.wav 
```



Il nome *soundName* è un segnaposto per un nome specificato per fare riferimento a questa risorsa WAVE. Le risorse WAVE vengono caricate e accessibili come altre risorse definite dall'Windows applicazione. La funzione PlayResource nell'esempio seguente riproduce una risorsa WAVE specificata.


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



Per riprodurre una risorsa WAVE usando questa funzione, passare alla funzione un puntatore a una stringa contenente il nome della risorsa, come illustrato nell'esempio seguente.


```C++
PlayResource("soundName"); 
```



 

 