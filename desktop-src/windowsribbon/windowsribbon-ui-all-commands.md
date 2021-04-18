---
title: UI_ALL_COMMANDS (UIRibbon. h)
description: Specifica una costante che identifica la raccolta di comandi dichiarati nel file di risorse di markup.
ms.assetid: b0046d8c-bb54-4231-90f0-c0b2c8790b1a
topic_type:
- apiref
api_name:
- UI_ALL_COMMANDS
api_location:
- Uiribbon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce287d6ee03734ecbb0dd84e020ec542a83f04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301399"
---
# <a name="ui_all_commands"></a>\_tutti i comandi dell'interfaccia utente \_

Specifica una costante che identifica la raccolta di comandi dichiarati nel file di risorse di markup.

## <a name="remarks"></a>Commenti

**Interfaccia utente \_ TUTTI i \_ comandi** sono utili quando è necessario accedere a proprietà simili in tutti i comandi. Ad esempio, **\_ tutti i \_ comandi dell'interfaccia utente** possono essere passati a [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) per invalidare e aggiornare tutti i comandi della barra multifunzione eseguendo una query sull'applicazione host per i nuovi valori delle proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma solo per le applicazioni desktop di Windows Vista \[\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma solo per le \[ app desktop Windows server 2008\]<br/> |
| Intestazione<br/>                   | <dl> <dt>UIRibbon. h</dt> </dl>                                             |
| IDL<br/>                      | <dl> <dt>UIRibbon. idl</dt> </dl>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti ed enumerazioni](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

