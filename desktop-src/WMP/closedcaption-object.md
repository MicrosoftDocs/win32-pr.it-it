---
title: Oggetto ClosedCaption
description: L'oggetto ClosedCaption fornisce un modo per includere le didascalie con una clip multimediale. Il testo della didascalia si trova in un file di interscambio multimediale accessibile sincronizzato (SAMI).
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- Media Player di Windows oggetto ClosedCaption
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85e53468e8d5cc2694555b9a05d8b207d1660618
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104045959"
---
# <a name="closedcaption-object"></a>Oggetto ClosedCaption

L'oggetto **ClosedCaption** fornisce un modo per includere le didascalie con una clip multimediale. Il testo della didascalia si trova in un file di interscambio multimediale accessibile sincronizzato (SAMI).

L'oggetto **ClosedCaption** supporta le proprietà seguenti.



| Proprietà                                           | Descrizione                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [captioningID](closedcaption-captioningid.md)     | Specifica o Recupera il nome del frame o del controllo che visualizza la didascalia.                   |
| [SAMIFileName](closedcaption-samifilename.md)     | Specifica o Recupera il nome del file contenente le informazioni necessarie per la didascalia chiusa. |
| [SAMILang](closedcaption-samilang.md)             | Specifica o recupera la lingua visualizzata per la didascalia chiusa.                                 |
| [SAMILangCount](closedcaption-samilangcount.md)   | Recupera il numero di lingue supportate dal file SAMI corrente.                                |
| [SAMIStyle](closedcaption-samistyle.md)           | Specifica o recupera lo stile dei sottotitoli codificati.                                                  |
| [SAMIStyleCount](closedcaption-samistylecount.md) | Recupera il numero di stili supportati dal file SAMI corrente.                                   |



 

L'oggetto **ClosedCaption** supporta i metodi seguenti.



| Metodo                                                 | Descrizione                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [getSAMILangID](closedcaption-getsamilangid.md)       | Recupera l'identificatore delle impostazioni locali (LCID) di una lingua supportata dal file SAMI corrente. |
| [getSAMILangName](closedcaption-getsamilangname.md)   | Recupera il nome di una lingua supportata dal file SAMI corrente.                     |
| [getSAMIStyleName](closedcaption-getsamistylename.md) | Recupera il nome di uno stile supportato dal file SAMI corrente.                        |



 

È possibile accedere all'oggetto **ClosedCaption** tramite la proprietà seguente.



| Oggetto                      | Proprietà                                  |
|-----------------------------|-------------------------------------------|
| [Player](player-object.md) | [closedCaption](player-closedcaption.md) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Aggiunta di didascalie chiuse a file multimediali digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Riferimento del modello a oggetti per lo scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




