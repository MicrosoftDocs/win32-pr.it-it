---
description: Valore che indica il tipo di sensore fornito da un'origine frame, ad esempio colore, a forma di rosso o profondità.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: MF_MT_FRAMESOURCE_TYPES attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3cddc28db050ec3fdb55e47ca2ceb1bd24fb2813bdf90fce439843957a7ae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113771"
---
# <a name="mf_mt_framesource_types-attribute"></a>Attributo MF \_ MT \_ FRAMESOURCE \_ TYPES

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Valore che indica il tipo di sensore fornito da un'origine frame, ad esempio colore, a forma di rosso o profondità.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo valore deve essere un membro [**\_ dell'enumerazione MFFrameSourceTypes.**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) Per compatibilità con le versioni precedenti, quando questo attributo non è definito in un tipo di supporto, si presuppone che sia **\_ MFFrameSourceTyes::Color**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                          |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                      |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
