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
# <a name="playing-wave-resources"></a>Riproduzione di risorse WAVE

È possibile usare la funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) per riprodurre un suono archiviato come risorsa. Sebbene sia possibile anche usare la funzione [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) , **sndPlaySound** richiede di trovare, caricare, bloccare, sbloccare e liberare la risorsa; **PlaySound** consente di ottenere tutti questi risultati con una sola riga di codice.

## <a name="playsound-example"></a>Esempio di PlaySound


```C++
PlaySound("SoundName", hInst, SND_RESOURCE | SND_ASYNC); 
```



## <a name="sndplaysound-example"></a>Esempio di sndPlaySound

Il \_ flag di memoria SND indica che il parametro *lpszSoundName* è un puntatore a un'immagine in memoria del file Wave. Per includere un file WAVE come risorsa in un'applicazione, aggiungere la voce seguente allo script di risorsa dell'applicazione (. RC) file.


```C++
soundName WAVE c:\sounds\bells.wav 
```



Il nome *soundName* è un segnaposto per il nome fornito per fare riferimento a questa risorsa Wave. Le risorse WAVE vengono caricate e accessibili in modo analogo alle altre risorse di Windows definite dall'applicazione. La funzione PlayResource nell'esempio seguente riproduce una risorsa WAVE specificata.


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



 

 