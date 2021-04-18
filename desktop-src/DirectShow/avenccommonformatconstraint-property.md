---
description: Specifica il formato di destinazione per un codificatore.
ms.assetid: 3d316561-352f-44f9-9978-01301a68e7b6
title: Proprietà AVEncCommonFormatConstraint (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e79536959aaaa0c50403bdd79d005bd48c729e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304246"
---
# <a name="avenccommonformatconstraint-property"></a>Proprietà AVEncCommonFormatConstraint

Specifica il formato di destinazione per un codificatore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCommonFormatConstraint**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un **BSTR** che contiene la rappresentazione di stringa di un GUID. Sono definiti i seguenti GUID.



| GUID                                         | Descrizione                     |
|----------------------------------------------|---------------------------------|
| \_GUID AVEncCommonFormatATSC di CODEcapi \_        | TV via cavo ATSC.          |
| \_GUID AVEncCommonFormatDVB di CODEcapi \_         | TV via cavo DVB.           |
| GUID di codecapi \_ \_ AVEncCommonFormatDVD \_ DashVR | DVD-VR                          |
| GUID di codecapi \_ \_ AVEncCommonFormatDVD \_ PlusVR | DVD + VR                          |
| GUID di codecapi \_ \_ AVEncCommonFormatDVD \_ V      | DVD-Video                       |
| \_GUID AVEncCommonFormatHighMAT di CODEcapi \_     | HighMAT                         |
| \_GUID AVEncCommonFormatHighMPV di CODEcapi \_     | Non documentato in questa versione. |
| \_GUID AVEncCommonFormatMP3 di CODEcapi \_         | Livello audio MPEG-3 (MP3)        |
| \_GUID AVEncCommonFormatSVCD di CODEcapi \_        | CD con video Super (SVCD)           |
| \_GUID AVEncCommonFormatUnSpecified di CODEcapi \_ | Formato non specificato.             |
| \_GUID AVEncCommonFormatVCD di CODEcapi \_         | CD video (VCD)                  |



 

## <a name="remarks"></a>Commenti

Le applicazioni possono impostare questa proprietà per specificare il formato di destinazione. I codificatori possono inoltre restituire questa proprietà come funzionalità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                     |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




