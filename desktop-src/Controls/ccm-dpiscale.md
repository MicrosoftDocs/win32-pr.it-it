---
title: CCM_DPISCALE messaggio (Commctrl.h)
description: Abilita il ridimensionamento automatico dei punti per pollice (dpi) in controlli Tree-View, controlli List-View, controlli ComboBoxEx, controlli Intestazione, pulsanti, controlli Barra degli strumenti, controlli Animazione ed Elenchi di immagini.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- CCM_DPISCALE di controllo Windows messaggio
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
ms.openlocfilehash: e7e72cb8ac3acf413e4381580a4ecf38a4f5bd4b2f5b03d6cff7d7abb85c1f0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320251"
---
# <a name="ccm_dpiscale-message"></a>Messaggio \_ CCM DPISCALE

Abilita il ridimensionamento automatico dei punti per pollice (dpi) nei controlli Visualizzazione albero [,](tree-view-controls.md)Controlli Visualizzazione elenco [,](list-view-control-reference.md) [Controlli ComboBoxEx](comboboxex-controls.md) [,](header-controls.md)controlli Intestazione , [Pulsanti](buttons.md) [,](toolbar-controls-overview.md)Controlli Barra [degli](animation-control-overview.md)strumenti , Controlli animazione ed Elenchi [immagini](image-lists.md).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Impostare su **TRUE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene usato.

## <a name="remarks"></a>Commenti

Avvio veloce e barra [delle applicazioni](/windows/desktop/shell/taskbar) non devono specificare un ridimensionamento dpi, perché le immagini sono già ridimensionate.

Qualsiasi controllo che usa un elenco di immagini creato con la metrica SmallIcon non deve ridimensionare le relative icone.

> [!Note]  
> Per usare questa API, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

