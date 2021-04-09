---
title: Messaggio di EM_GETAUTOURLDETECT (RichEdit. h)
description: Indica se il rilevamento URL automatico è attivato nel controllo Rich Edit.
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- Controlli di Windows Message EM_GETAUTOURLDETECT
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e68e4f2991c5f8780cb587594289674e07ec992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048449"
---
# <a name="em_getautourldetect-message"></a>\_Messaggio GETAUTOURLDETECT em

Indica se il rilevamento URL automatico è attivato nel controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il rilevamento URL automatico è attivo, il valore restituito è 1.

Se il rilevamento URL automatico è inattivo, il valore restituito è 0.

## <a name="remarks"></a>Commenti

Quando il rilevamento URL automatico è acceso, Microsoft Rich Edit controlla costantemente il testo tipizzato per un URL valido. Rich Edit riconosce gli URL che iniziano con i prefissi seguenti:

-   http:
-   file:
-   mailto:
-   FTP
-   https
-   Gopher
-   NNTP
-   Prospero
-   Telnet
-   Notizie
-   WAIS
-   Outlook

Rich Edit riconosce inoltre i nomi di percorso standard che iniziano con \\ \\ . Quando Rich Edit individua un URL, modifica il colore del testo dell'URL, sottolinea il testo e invia una notifica al client usando il [ \_ collegamento it](en-link.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_collegamento en](en-link.md)
</dt> </dl>

 

 





