---
title: Altri attributi predefiniti (TsAttrid. h)
description: I valori seguenti identificano gli attributi vari ottenuti con il metodo GetAppProperty di ITfContext. Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.
ms.assetid: 8536938b-98a1-415b-b5f2-45b90215c270
keywords:
- Altri attributi predefiniti Framework servizi di testo
topic_type:
- apiref
api_name:
- Other Predefined Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d0a3ff72a5ea84a6b9e5b47106012a945dbf45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302244"
---
# <a name="other-predefined-attributes"></a>Altri attributi predefiniti

I valori seguenti identificano gli attributi vari ottenuti con il metodo [ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.

## <a name="properties"></a>Proprietà



| Proprietà                             | Descrizione                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------|
| **\_App TSATTRID**                    | Non usato.                                                                         |
| **\_App TSATTRID \_ IncorrectGrammar**  | Contiene un valore diverso da zero se il testo contiene un errore di grammatica o zero in caso contrario.  |
| **\_App TSATTRID \_ IncorrectSpelling** | Contiene un valore diverso da zero se il testo contiene un errore di ortografia o zero in caso contrario. |
| **TSATTRID \_ altri**                 | Non usato.                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>TsAttrid. h</dt> </dl> |



 

