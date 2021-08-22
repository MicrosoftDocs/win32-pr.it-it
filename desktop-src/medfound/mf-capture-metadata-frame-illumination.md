---
description: Valore che indica se un fotogramma è stato acquisito utilizzando l'illuminazione a ir (IR) attiva.
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: MF_CAPTURE_METADATA_FRAME_ILLUMINATION attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23658f8f396a81180a074badc43e98d0f392fc355c1a81a4d1e731d132de12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973950"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a>Attributo MF \_ CAPTURE \_ METADATA FRAME \_ \_ ILLUMINATION

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Valore che indica se un fotogramma è stato acquisito utilizzando l'illuminazione a ir (IR) attiva.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

Questo attributo è una maschera di bit. È un valore a 64 bit per la compatibilità con le versioni precedenti.

L'illuminazione attiva si verifica quando un dispositivo ha un emettitore di luce vicino alla fotocamera di IR che emette un trasmettitore di luce per illuminare la scena, in genere emettendo luce AR in modo da non intasare gli occhi umani. Impostare il valore su (valore & 0x1) != 0 se il fotogramma è stato acquisito quando l'illuminazione attiva era attiva e impostato (valore & 0x1) == 0 se l'illuminazione attiva era disattivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                      |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




