---
title: Funzioni di calibrazione e caratterizzazione dei dispositivi
description: Le funzioni seguenti sono utili per la scrittura di strumenti di calibrazione e caratterizzazione dei dispositivi necessari per l'installazione e la calibrazione di dispositivi di visualizzazione a colori, ad esempio monitor e stampanti.
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Windows Sistema di colori (WCS), funzioni
- WCS (Windows Color System), funzioni
- gestione del colore delle immagini, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Informazioni di riferimento su WCS, funzioni
- informazioni di riferimento per WCS, funzioni
- Windows Sistema a colori (WCS), calibrazione del dispositivo
- WCS (Windows Color System), calibrazione del dispositivo
- gestione del colore delle immagini, calibrazione del dispositivo
- gestione del colore, calibrazione del dispositivo
- colori, calibrazione del dispositivo
- Informazioni di riferimento su WCS, calibrazione del dispositivo
- informazioni di riferimento per WCS, calibrazione del dispositivo
- Windows Sistema di colori (WCS), caratterizzazione
- WCS (Windows Color System), caratterizzazione
- gestione del colore delle immagini, caratterizzazione
- gestione dei colori, caratterizzazione
- colori, caratterizzazione
- Informazioni di riferimento su WCS, caratterizzazione
- informazioni di riferimento per WCS, caratterizzazione
- calibrazione del dispositivo
- Calibrazione
- Caratterizzazione
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aea24f0a1e033df62c70674c44c9b5e9c6c0e0de1011b9ea95b9e5389d6004c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452027"
---
# <a name="device-calibration-and-characterization-functions"></a>Funzioni di calibrazione e caratterizzazione dei dispositivi

Le funzioni seguenti sono utili per la scrittura di strumenti di calibrazione e caratterizzazione dei dispositivi necessari per l'installazione e la calibrazione di dispositivi di visualizzazione a colori, ad esempio monitor e stampanti.



| Funzione | Descrizione |
|-|-|
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Chiude un handle di profilo aperto. |
| [**CreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | Crea un profilo di collegamento del dispositivo ICC (International Color *Consortium)* da un set di profili colori, usando le finalità specificate. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Copia i dati da un elemento del profilo con tag specificato di un profilo colori specificato in un buffer. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Recupera il nome del tag specificato da *dwIndex* nella tabella dei tag di un profilo colori ICC (International Color Consortium) specificato, dove *dwIndex* è un indice in base uno in tale tabella. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| Recupera il contenuto del profilo colori dato un handle per un profilo colori aperto.     |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Recupera o deriva la struttura dell'intestazione ICC dal profilo colori ICC o dal profilo XML WCS. I driver e le applicazioni devono presupporre che la restituzione **di TRUE** indichi solo che viene restituita un'intestazione strutturata correttamente. Ogni tag dovrà comunque essere convalidato in modo indipendente usando le API ICM2 legacy o LE API di XML Schema. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Recupera il numero di elementi contrassegnati in un profilo colori specificato. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Recupera il dizionario PostScript rendering colori di livello 2 dal profilo colori ICC specificato. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Recupera la finalità PostScript [rendering](r.md) dei colori di livello 2 da un profilo colori ICC. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Recupera la matrice PostScript spazio [colori](c.md) di livello 2 da un profilo colori ICC. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Indica se un tag ICC (International Color Consortium) specificato è presente nel profilo colori specificato. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Consente di determinare se il profilo specificato è un profilo ICC (International Color Consortium) valido o un handle di profilo WCS (Windows Color System) valido che può essere usato per la gestione del colore. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Crea un handle per un profilo colori specificato. L'handle può quindi essere usato in altre funzioni di gestione dei profili. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Imposta i dati dell'elemento per un elemento del profilo con tag in un profilo colori ICC. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Crea in un profilo colori ICC specificato un nuovo tag che fa riferimento agli stessi dati di un tag esistente. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Imposta le dimensioni di un elemento con tag in un profilo colori ICC. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Imposta i dati dell'intestazione in un profilo colori ICC specificato. |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Determina se la gestione del sistema dello stato di calibrazione dello schermo è abilitata. |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Determina se la gestione del sistema dello stato di calibrazione dello schermo è abilitata. |



 

 

 




