---
title: Funzioni di calibratura e di caratterizzazione del dispositivo
description: Le funzioni seguenti sono utili per la scrittura di strumenti di calibratura e di caratterizzazione dei dispositivi necessari per installare e calibrare i dispositivi di visualizzazione dei colori, ad esempio monitoraggi e stampanti.
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Windows Color System (WCS), funzioni
- WCS (Windows Color System), funzioni
- Gestione colori immagine, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Riferimento a WCS, funzioni
- informazioni di riferimento su WCS, funzioni
- Windows Color System (WCS), calibrazione del dispositivo
- WCS (sistema di colori Windows), calibrazione del dispositivo
- Gestione colori immagine, calibrazione dispositivo
- gestione dei colori, calibrazione del dispositivo
- colori, calibrazione del dispositivo
- Riferimento a WCS, calibrazione del dispositivo
- informazioni di riferimento per WCS, calibrazione del dispositivo
- Sistema di colori Windows (WCS), caratterizzazione
- WCS (sistema di colori Windows), caratterizzazione
- Gestione colori immagine, caratterizzazione
- gestione dei colori, caratterizzazione
- colori, caratterizzazione
- Riferimento a WCS, caratterizzazione
- informazioni di riferimento su WCS, caratterizzazione
- calibrazione del dispositivo
- calibrazione
- caratterizzazione
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367bbc6385cc21c8dbff3a88bed685616fb3f29
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322035"
---
# <a name="device-calibration-and-characterization-functions"></a>Funzioni di calibratura e di caratterizzazione del dispositivo

Le funzioni seguenti sono utili per la scrittura di strumenti di calibratura e di caratterizzazione dei dispositivi necessari per installare e calibrare i dispositivi di visualizzazione dei colori, ad esempio monitoraggi e stampanti.



| Funzione | Descrizione |
|-|-|
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Chiude un handle del profilo aperto. |
| [**CreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | Crea un *profilo di collegamento del dispositivo* ICC (International Color Consortium) da un set di profili colori, usando gli Intent specificati. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Copia i dati da un elemento profilo con tag specificato di un profilo colori specificato in un buffer. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Recupera il nome del tag specificato da *dwIndex* nella tabella dei tag di un profilo colori ICC (International Color Consortium) specificato, in cui *dwIndex* è un indice in base uno in tale tabella. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| Recupera il contenuto del profilo colori dato un handle a un profilo colori aperto.     |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Recupera o deriva la struttura di intestazione ICC da profilo colori ICC o dal profilo XML WCS. I driver e le applicazioni devono presupporre che restituisca **true** solo indica che viene restituita un'intestazione strutturata correttamente. Ogni tag dovrà comunque essere convalidato in modo indipendente usando API ICM2 legacy o API XML Schema. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Recupera il numero di elementi contrassegnati in un profilo colori specificato. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Recupera il dizionario per il rendering del colore di livello 2 PostScript dal profilo colori ICC specificato. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Recupera lo [scopo del rendering](r.md) dei colori a livello 2 del post-script da un profilo colori ICC. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Recupera la matrice di spazi dei [colori](c.md) di livello 2 PostScript da un profilo colori ICC. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Indica se nel profilo colori specificato è presente un tag ICC (International Color Consortium) specificato. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Consente di determinare se il profilo specificato è un profilo ICC (International Color Consortium) valido o un handle del profilo WCS (Windows Color System) valido che può essere utilizzato per la gestione dei colori. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Crea un handle per un profilo colori specificato. L'handle può quindi essere utilizzato in altre funzioni di gestione dei profili. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Imposta i dati dell'elemento per un elemento del profilo con tag in un profilo colori ICC. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Crea in un profilo colori ICC specificato un nuovo tag che fa riferimento agli stessi dati di un tag esistente. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Imposta la dimensione di un elemento con tag in un profilo colori ICC. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Imposta i dati dell'intestazione in un profilo colori ICC specificato. |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Determina se è abilitata la gestione del sistema dello stato di calibrazione dello schermo. |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Determina se è abilitata la gestione del sistema dello stato di calibrazione dello schermo. |



 

 

 




