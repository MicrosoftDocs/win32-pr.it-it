---
title: UI_ALL_COMMANDS (Uiribbon.h)
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
ms.openlocfilehash: 24767f2d3839b94ee83c6a9a527b2e80dcf8c1960e877f65a0e7e96fff4e3ec4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705960"
---
# <a name="ui_all_commands"></a>TUTTI I \_ COMANDI \_ DELL'INTERFACCIA UTENTE

Specifica una costante che identifica la raccolta di comandi dichiarati nel file di risorse di markup.

## <a name="remarks"></a>Commenti

**Interfaccia utente \_ ALL \_ COMMANDS** è utile quando è necessario accedere a proprietà simili in tutti i comandi. Ad esempio, è possibile passare **UI \_ ALL \_ COMMANDS** a [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) per invalidare e aggiornare tutti i comandi della barra multifunzione tramite una query sull'applicazione host per i nuovi valori delle proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e Aggiornamento piattaforma solo per Windows app desktop vista \[\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma solo per Windows server 2008 \[ desktop\]<br/> |
| Intestazione<br/>                   | <dl> <dt>Uiribbon.h</dt> </dl>                                             |
| Idl<br/>                      | <dl> <dt>Uiribbon.idl</dt> </dl>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti ed enumerazioni](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

