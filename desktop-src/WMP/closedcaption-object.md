---
title: Oggetto ClosedCaption
description: L'oggetto ClosedCaption consente di includere didascalie con un clip multimediale. Il testo dei sottotitoli si trova in un file SAMI (Synchronized Accessible Media Interchange).
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- Oggetto ClosedCaption Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10ae51af31e724bd066dbbb9e826569da40159460eb1e7bf570aea331dff86be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119595"
---
# <a name="closedcaption-object"></a>Oggetto ClosedCaption

**L'oggetto ClosedCaption** consente di includere didascalie con un clip multimediale. Il testo dei sottotitoli si trova in un file SAMI (Synchronized Accessible Media Interchange).

**L'oggetto ClosedCaption** supporta le proprietà seguenti.



| Proprietà                                           | Descrizione                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [captioningID](closedcaption-captioningid.md)     | Specifica o recupera il nome del frame o del controllo che visualizza la didascalia.                   |
| [SAMIFileName](closedcaption-samifilename.md)     | Specifica o recupera il nome del file contenente le informazioni necessarie per i sottotitoli codificati. |
| [SAMILang](closedcaption-samilang.md)             | Specifica o recupera la lingua visualizzata per i sottotitoli codificati.                                 |
| [SAMILangCount](closedcaption-samilangcount.md)   | Recupera il numero di lingue supportate dal file SAMI corrente.                                |
| [SAMIStyle](closedcaption-samistyle.md)           | Specifica o recupera lo stile di sottotitoli codificati.                                                  |
| [SAMIStyleCount](closedcaption-samistylecount.md) | Recupera il numero di stili supportati dal file SAMI corrente.                                   |



 

**L'oggetto ClosedCaption** supporta i metodi seguenti.



| Metodo                                                 | Descrizione                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [getSAMILangID](closedcaption-getsamilangid.md)       | Recupera l'identificatore delle impostazioni locali (LCID) di una lingua supportata dal file SAMI corrente. |
| [getSAMILangName](closedcaption-getsamilangname.md)   | Recupera il nome di una lingua supportata dal file SAMI corrente.                     |
| [getSAMIStyleName](closedcaption-getsamistylename.md) | Recupera il nome di uno stile supportato dal file SAMI corrente.                        |



 

**L'oggetto ClosedCaption** è accessibile tramite la proprietà seguente.



| Oggetto                      | Proprietà                                  |
|-----------------------------|-------------------------------------------|
| [Player](player-object.md) | [closedCaption](player-closedcaption.md) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di sottotitoli codificati ai supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Informazioni di riferimento sul modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




