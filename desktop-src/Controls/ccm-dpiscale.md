---
title: Messaggio CCM_DPISCALE (COMmctrl. h)
description: Consente la scalabilità di punti per pollice (dpi) automatica in Tree-View controlli, controlli List-View, controlli ComboBoxEx, controlli Header, pulsanti, controlli della barra degli strumenti, controlli di animazione ed elenchi di immagini.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- Controlli di Windows Message CCM_DPISCALE
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120330"
---
# <a name="ccm_dpiscale-message"></a>\_Messaggio DPISCALE CCM

Consente il ridimensionamento DPI (punti per pollice) automatico per i controlli di [visualizzazione albero](tree-view-controls.md), i [controlli visualizzazione elenco](list-view-control-reference.md), i controlli [ComboBoxEx](comboboxex-controls.md), i [controlli intestazione](header-controls.md), i [pulsanti](buttons.md), i controlli della [barra degli strumenti](toolbar-controls-overview.md), i [controlli di animazione](animation-control-overview.md)e gli [elenchi di immagini](image-lists.md).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Impostare su **true**.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="remarks"></a>Commenti

L'avvio veloce e la [barra delle applicazioni](/windows/desktop/shell/taskbar) non devono specificare una scala dpi, perché le immagini sono già ridimensionate.

Qualsiasi controllo che usa un elenco di immagini creato con la metrica SmallIcon non deve ridimensionare le proprie icone.

> [!Note]  
> Per usare questa API, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

