---
title: Funzioni avanzate da usare all'esterno di un contesto di dispositivo
description: Queste funzioni forniscono funzionalità avanzate di gestione dei colori all'esterno dei contesti di dispositivo.
ms.assetid: 2f742743-094a-44b8-816b-24246607caeb
keywords:
- Windows Color System (WCS), funzioni
- WCS (Windows Color System), funzioni
- Gestione colori immagine, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Riferimento a WCS, funzioni
- informazioni di riferimento su WCS, funzioni
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04b7afe98f468fd3f580adf3eff145bce3aa1ac
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320203"
---
# <a name="advanced-functions-for-use-outside-of-a-device-context"></a>Funzioni avanzate da usare all'esterno di un contesto di dispositivo

Queste funzioni forniscono funzionalità avanzate di gestione dei colori all'esterno dei contesti di dispositivo.



| Funzione                                                           | Descrizione                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (o **ApplyCallbackFunction**) è una funzione di callback implementata che aggiorna i dati di configurazione di WCS mentre è in esecuzione la finestra di dialogo visualizzata dalla funzione [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) . |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Verifica se i pixel in una bitmap specificata si trovano all'interno del [gamut](g.md) di output di una trasformazione specificata. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Determina se i colori in una matrice si trovano all'interno del [gamut](g.md) di output di una trasformazione specificata. |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Converte i nomi di colore in uno spazio di colore denominato per indicizzare i numeri in un profilo colori ICC (International Color Consortium). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Trasforma gli indici in uno spazio colore in una matrice di nomi in uno spazio dei colori denominato. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Trasforma gli indici in uno spazio colore in una matrice di nomi in uno spazio dei colori denominato. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Accetta una matrice di profili o un singolo [profilo di collegamento del dispositivo](d.md) e crea una trasformazione colore che le applicazioni possono usare per eseguire il mapping dei colori. |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Elimina una trasformazione colore specificata. |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Recupera varie informazioni sul modulo di gestione colori (CMM) che ha creato la trasformazione colore specificata. |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Recupera le informazioni sul profilo colori International Color Consortium (ICC) indicato nel primo parametro. |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)         | Funzione di callback fornita dall'applicazione per segnalare lo stato di avanzamento. Il nome di questa funzione viene definito anche dall'applicazione.                                                 |
| [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) | Consente di selezionare il modulo di gestione colori (CMM) preferito da usare. |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                   | Fornisce il controllo utente sulla gestione dei colori tramite una finestra di dialogo.                                                                                                      |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                 | Converte i colori bitmap utilizzando una trasformazione colore.                                                                                                                          |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Converte una matrice di colori dallo [spazio del colore](c.md) di origine allo spazio dei colori di destinazione in base a quanto definito da una trasformazione colore. |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                           | Determina se i colori in una matrice si trovano all'interno del gamut di output di una trasformazione del colore WCS specificata.                                                                |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Converte una matrice di colori dallo spazio del colore di origine allo spazio dei colori di destinazione in base a quanto definito da una trasformazione colore.                                                |



 

 

 




