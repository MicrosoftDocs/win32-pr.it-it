---
title: Messaggio di EM_GETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Restituisce lo stato corrente delle opzioni tipografiche di un controllo Rich Edit.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- Controlli di Windows Message EM_GETTYPOGRAPHYOPTIONS
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d692639ba6c8cea758abe694faed3a46e3f65be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120722"
---
# <a name="em_gettypographyoptions-message"></a>\_Messaggio GETTYPOGRAPHYOPTIONS em

Restituisce lo stato corrente delle opzioni tipografiche di un controllo Rich Edit.

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

Restituisce le opzioni di tipografia correnti. Per un elenco di opzioni, vedere [**em \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).

## <a name="remarks"></a>Commenti

È possibile attivare l'interruzioni di riga avanzate inviando il messaggio [**\_ SETTYPOGRAPHYOPTIONS em**](em-settypographyoptions.md) . Le interruzioni di riga avanzate e normali possono anche essere attivate automaticamente dal controllo Rich Edit, se necessario per determinate lingue.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | Modifica avanzata 3,0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_SETTYPOGRAPHYOPTIONS em**](em-settypographyoptions.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sui controlli Rich Edit](about-rich-edit-controls.md)
</dt> </dl>

 

 





