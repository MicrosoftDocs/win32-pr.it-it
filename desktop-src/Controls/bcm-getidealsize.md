---
title: Messaggio BCM_GETIDEALSIZE (COMmctrl. h)
description: Ottiene le dimensioni del pulsante che meglio si adatta al testo e all'immagine, se è presente un elenco di immagini. È possibile inviare questo messaggio in modo esplicito o usare il pulsante \_ GetIdealSize macro.
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- Controlli di Windows Message BCM_GETIDEALSIZE
topic_type:
- apiref
api_name:
- BCM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446f4acba39b8b9722ef1a01a223f671b56ae845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301588"
---
# <a name="bcm_getidealsize-message"></a>\_Messaggio GETIDEALSIZE BCM

Ottiene le dimensioni del pulsante che meglio si adatta al testo e all'immagine, se è presente un elenco di immagini. È possibile inviare questo messaggio in modo esplicito o usare il [**pulsante \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) che riceve la dimensione desiderata del pulsante, incluso il testo e l'elenco delle immagini, se presente. L'applicazione chiamante è responsabile dell'allocazione di questa struttura. Impostare i membri **CX** e **CY** su zero per avere l'altezza e la larghezza ideali restituite nella struttura delle **dimensioni** . Per specificare la larghezza di un pulsante, impostare il membro **CX** sulla larghezza desiderata per il pulsante. Il sistema calcolerà l'altezza ideale per questa larghezza e la restituirà nel membro **CY** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, restituisce **true**. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

> [!Note]  
> Se non si desidera la larghezza del pulsante speciale, è necessario impostare entrambi i membri della [**dimensione**](/previous-versions//dd145106(v=vs.85)) su zero per calcolare e restituire l'altezza e la larghezza ideali. Se il valore del membro **CX** è maggiore di zero, questo valore viene considerato la larghezza desiderata del pulsante e l'altezza ideale per questa larghezza viene calcolata e restituita nel membro **CY** .

 

Questo messaggio è più applicabile ai pulsanti. Quando viene inviato a un pulsante, il messaggio recupera il rettangolo di delimitazione necessario per visualizzare il testo del pulsante. Inoltre, se il pulsante ha un elenco di immagini, anche il rettangolo di delimitazione viene ridimensionato in modo da includere l'immagine del pulsante.

Quando viene inviato a un pulsante di qualsiasi altro tipo, vengono recuperate le dimensioni del rettangolo della finestra del controllo.

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

