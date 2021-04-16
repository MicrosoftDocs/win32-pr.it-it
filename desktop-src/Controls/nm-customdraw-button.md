---
title: Codice di notifica di NM_CUSTOMDRAW (Button) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo Button informazioni sulle operazioni di disegni personalizzate sul pulsante. Il controllo Button invia questo codice di notifica sotto forma di messaggio di \_ notifica WM.
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- NM_CUSTOMDRAW (pulsante) codice di notifica controlli Windows
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab3cc4eb73c3a0185131bb6ef2198458888ec89d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479426"
---
# <a name="nm_customdraw-button-notification-code"></a>\_Codice di notifica CUSTOMDRAW (Button) Nm

Notifica alla finestra padre di un controllo Button informazioni sulle operazioni di disegni personalizzate sul pulsante.

Il controllo Button invia questo codice di notifica sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) che contiene informazioni sull'operazione di disegno. Il membro **dwItemSpec** di questa struttura contiene l'indice dell'elemento da disegnare e il membro **lItemlParam** di questa struttura contiene l'elemento *lParam* dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente. Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno. È necessario restituire uno dei valori seguenti.



| Codice restituito                                                                                          | Descrizione                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_NOTIFYPOSTERASE CDRF**</dt> </dl> | Il controllo invierà una notifica al padre dopo la cancellazione di un elemento. Questa operazione può essere utilizzata solo se **dwDrawStage** è uguale a CDDS \_ preerase.<br/>                                  |
| <dl> <dt>**\_NOTIFYPOSTPAINT CDRF**</dt> </dl> | Il controllo invierà una notifica al padre dopo aver disegnato un elemento. Può essere usato solo se **dwDrawStage** è uguale a CDDS \_ PrePaint.<br/>                                 |
| <dl> <dt>**\_SKIPDEFAULT CDRF**</dt> </dl>     | L'applicazione ha disegnato manualmente l'elemento. L'elemento non viene disegnato dal controllo. Questa operazione può essere usata quando **dwDrawStage** è uguale a CDDS \_ PREerase o CDDS \_ nonpaint.<br/> |



 

## <a name="remarks"></a>Commenti

Se il controllo Button è contrassegnato come OwnerDraw (BS \_ OwnerDraw), il \_ codice di notifica CUSTOMDRAW nm non viene inviato.

Per ulteriori informazioni, vedere [utilizzo del progetto personalizzato](custom-draw.md) .

> [!Note]  
> Per usare questo codice di notifica, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h (include Windows. h)</dt> </dl> |



 

 





