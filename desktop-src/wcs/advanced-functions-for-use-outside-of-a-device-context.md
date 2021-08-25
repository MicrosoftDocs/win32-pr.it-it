---
title: Funzioni avanzate per l'uso all'esterno di un contesto di dispositivo
description: Queste funzioni forniscono funzionalità avanzate di gestione del colore al di fuori dei contesti di dispositivo.
ms.assetid: 2f742743-094a-44b8-816b-24246607caeb
keywords:
- Windows Sistema di colori (WCS), funzioni
- WCS (Windows Color System), funzioni
- gestione del colore delle immagini, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Informazioni di riferimento su WCS, funzioni
- informazioni di riferimento per WCS, funzioni
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685b9fe1c7139be1c54e1b158a03c1de54d01b2b80ec4cab4b86603680c6d957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814616"
---
# <a name="advanced-functions-for-use-outside-of-a-device-context"></a>Funzioni avanzate per l'uso all'esterno di un contesto di dispositivo

Queste funzioni forniscono funzionalità avanzate di gestione del colore al di fuori dei contesti di dispositivo.



| Funzione                                                           | Descrizione                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (o **ApplyCallbackFunction**) è una funzione di callback implementata che aggiorna i dati di configurazione WCS durante l'esecuzione della finestra di dialogo visualizzata dalla funzione [**SetupColorMatchingW.**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Controlla se i pixel in una bitmap specificata si trovano all'interno della [gamma di](g.md) output di una trasformazione specificata. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Determina se i colori di una matrice si trovano all'interno della [gamma di](g.md) output di una trasformazione specificata. |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Converte i nomi dei colori in uno spazio colore denominato in numeri di indice in un profilo colori ICC (International Color Consortium). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Trasforma gli indici in uno spazio colori in una matrice di nomi in uno spazio colori denominato. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Trasforma gli indici in uno spazio colori in una matrice di nomi in uno spazio colori denominato. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Accetta una matrice di profili o un singolo profilo di collegamento [del](d.md) dispositivo e crea una trasformazione colore che le applicazioni possono usare per eseguire il mapping dei colori. |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Elimina una trasformazione di colore specificata. |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Recupera varie informazioni sul modulo di gestione colori (CMM) che ha creato la trasformazione del colore specificata. |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Recupera informazioni sul profilo colori denominato ICC (International Color Consortium) specificato nel primo parametro. |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)         | Funzione di callback fornita dall'applicazione per segnalare lo stato di avanzamento. Anche il nome di questa funzione è definito dall'applicazione.                                                 |
| [**Selezionare CMM**](/windows/win32/api/icm/nf-icm-selectcmm) | Consente di selezionare il modulo CMM (Color Management Module) preferito da usare. |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                   | Fornisce il controllo utente sulla gestione del colore tramite una finestra di dialogo.                                                                                                      |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                 | Converte i colori bitmap usando una trasformazione di colore.                                                                                                                          |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Converte una matrice di colori dallo spazio [colori di origine](c.md) allo spazio colori di destinazione come definito da una trasformazione di colore. |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                           | Determina se i colori in una matrice sono all'interno della gamma di output di una trasformazione di colori WCS specificata.                                                                |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Converte una matrice di colori dallo spazio colori di origine allo spazio colori di destinazione come definito da una trasformazione di colore.                                                |



 

 

 




