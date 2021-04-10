---
title: Attributi elenco predefiniti (TsAttrid. h)
description: I valori seguenti identificano gli attributi dell'elenco ottenuti con il metodo ITfContext GetAppProperty. Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- Framework dei servizi di testo attributi elenco predefiniti
topic_type:
- apiref
api_name:
- Predefined List Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ade2403e124b934c6872f39c01fc7fc1ea6f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120907"
---
# <a name="predefined-list-attributes"></a>Attributi elenco predefiniti

I valori seguenti identificano gli attributi dell'elenco ottenuti con il metodo [ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.

## <a name="properties"></a>Proprietà



| Proprietà                          | Descrizione                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| \_Elenco TSATTRID                    | Non usato.                                                                                       |
| \_Elenco TSATTRID \_ LevelIndel        | Contiene il livello di indice dell'elenco. 1 è il livello più esterno, 2 è il livello successivo e così via. |
| \_Tipo di elenco TSATTRID \_              | Non usato.                                                                                       |
| \_Tipo di elenco TSATTRID \_ \_ arabo      | Contiene un valore diverso da zero se l'elenco è un elenco di numeri arabi o zero in caso contrario.               |
| \_Elenco TSATTRID \_ tipo \_ elenco      | Contiene un valore diverso da zero se l'elenco è un elenco puntato o zero in caso contrario.                      |
| \_Tipo di elenco TSATTRID \_ \_ LowerLetter | Contiene un valore diverso da zero se l'elenco è un elenco con lettere minuscole o zero in caso contrario.            |
| \_Tipo di elenco TSATTRID \_ \_ LowerRoman  | Contiene un valore diverso da zero se l'elenco è un elenco di numeri romani minuscoli oppure zero in caso contrario.       |
| \_Tipo di elenco TSATTRID \_ \_ UpperLetter | Contiene un valore diverso da zero se l'elenco è un elenco con lettere maiuscole o zero in caso contrario.          |
| \_Tipo di elenco TSATTRID \_ \_ UpperRoman  | Contiene un valore diverso da zero se l'elenco è un elenco di numeri romani in maiuscolo o zero in caso contrario.      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>TsAttrid. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

