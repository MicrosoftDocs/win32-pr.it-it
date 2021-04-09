---
description: Specifica il profilo di complessità del contenuto codificato.
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: Proprietà MFPKEY_DECODERCOMPLEXITYPROFILE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39544830a0a05e21779a637da61d3bcb310fcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880818"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a>\_Proprietà DECODERCOMPLEXITYPROFILE di MFPKEY

Specifica il profilo di complessità del contenuto codificato.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCDecoderComplexityProfile

## <a name="data-type"></a>Tipo di dati

**\_BSTR VT**

## <a name="remarks"></a>Commenti

È possibile leggere questo valore solo dopo il completamento della codifica.

Per l'audio, questa proprietà ha uno dei valori seguenti.



| Valore | Descrizione                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| L1  | Codifica standard con frequenza di campionamento pari a 44,1 KHz e velocità in bit massima di 161 kbps.         |
| L2  | Codifica standard con frequenze di campionamento fino a 48 KHz e velocità in bit massima di 161 kbps.         |
| L3  | Codifica standard con frequenze di campionamento fino a 48 KHz e velocità in bit massima di 385 kbps.         |
| "M0a" | Codifica professionale con frequenze di campionamento fino a 48 KHz e velocità in bit comprese tra 48 e 192 kbps.  |
| "M0b" | Codifica professionale con frequenza di campionamento fino a 48 KHz e velocità in bit massima di 192 kbps.      |
| M1  | Codifica professionale con frequenza di campionamento fino a 48 KHz e velocità in bit massima di 384 kbps.      |
| M2  | Codifica professionale con frequenza di campionamento fino a 96 KHz e velocità in bit massima di 768 kbps.      |
| M3  | Codifica professionale con frequenza di campionamento fino a 96 KHz e velocità in bit massima di 1,5 Mbps.      |
| N1  | Codifica senza perdita di frequenza con frequenze di campionamento fino a 48 KHz e un massimo di 2 canali.                |
| N2  | Codifica senza perdita di frequenza con frequenze di campionamento fino a 96 KHz e un massimo di 6 canali (surround 5,1). |
| N3  | Codifica senza perdita di frequenza con frequenze di campionamento fino a 96 KHz e un massimo di 8 canali (7,1 surround). |



 

Per il video, questa proprietà ha uno dei valori seguenti:



| Valore | Descrizione                                                                       |
|-------|-----------------------------------------------------------------------------------|
| Asia Pacifico  | profilo avanzato (disponibile solo in Windows Media Video 9 Advanced Profile codec) |
| CP  | non più supportato                                                               |
| MP  | profilo principale                                                                      |
| SP  | Profilo semplice                                                                    |



 

Per il contenuto video, è possibile richiedere un livello di profilo impostando [MFPKEY \_ DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) prima di iniziare la codifica. Il codec tenterà di codificare entro i parametri del livello di complessità richiesto, ma le altre impostazioni configurate avranno la precedenza. È consigliabile controllare sempre il valore del profilo di complessità effettivo dopo la codifica nel caso in cui non sia possibile rispettare la richiesta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




