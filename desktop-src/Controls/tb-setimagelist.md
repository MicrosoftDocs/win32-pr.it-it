---
title: TB_SETIMAGELIST messaggio (Commctrl.h)
description: Imposta l'elenco di immagini utilizzato dalla barra degli strumenti per visualizzare i pulsanti nello stato predefinito.
ms.assetid: 432ffdfc-bb63-4405-90da-9392910fdbb6
keywords:
- TB_SETIMAGELIST dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a7110084f2abe39cbae51815d1e59972cb016ea267275f0481d21e1f8b908a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167461"
---
# <a name="tb_setimagelist-message"></a>TB \_ SETIMAGELIST message

Imposta l'elenco di immagini utilizzato dalla barra degli strumenti per visualizzare i pulsanti nello stato predefinito.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[Versione 5.80.](common-control-versions.md) Indice dell'elenco. Se si usa un solo elenco di immagini o una versione precedente dei controlli comuni, impostare *wParam* su zero. Per informazioni dettagliate sull'uso di più elenchi di immagini, vedere Osservazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elenco di immagini da impostare. Se questo parametro è **NULL,** nei pulsanti non viene visualizzata alcuna immagine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle all'elenco di immagini utilizzato in precedenza per visualizzare i pulsanti nello stato predefinito oppure **NULL se** in precedenza non è stato impostato alcun elenco di immagini.

## <a name="remarks"></a>Commenti

> [!Note]  
> L'applicazione è responsabile della rimozione dell'elenco di immagini dopo l'eliminazione della barra degli strumenti.

 

Il **messaggio \_ SETIMAGELIST** tb non può essere combinato con [**TB \_ ADDBITMAP.**](tb-addbitmap.md) Non può inoltre essere usato con le barre degli strumenti create con [**CreateToolbarEx,**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)che chiama **\_ INTERNAMENTE TB ADDBITMAP.** Quando si crea una barra degli strumenti con **CreateToolbarEx** o si usa **\_ TB ADDBITMAP** per aggiungere immagini, la barra degli strumenti gestisce internamente l'elenco di immagini. Il tentativo di modificarlo con **\_ SETIMAGELIST tb** ha conseguenze imprevedibili.

Con [la versione 5.80](common-control-versions.md) o successiva dei controlli comuni, le immagini dei pulsanti non devono derivare dallo stesso elenco di immagini. Per usare più elenchi di immagini per le immagini dei pulsanti della barra degli strumenti:

1.  Abilitare più elenchi di immagini inviando alla barra degli strumenti un messaggio [**\_ CCM SETVERSION**](ccm-setversion.md) con *wParam* (numero di versione) impostato su 5.
2.  Per ogni elenco di immagini da usare, inviare alla barra degli strumenti un messaggio **\_ SETIMAGELIST da TB.** Impostare *wParam* su un valore *wParam* definito dall'applicazione che verrà usato per identificare l'elenco. Impostare *lParam* sull'handle HIMAGELIST dell'elenco.
3.  Per ogni pulsante, impostare il membro **iBitmap** della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) del pulsante su MAKELONG(*iIndex*, *iImageID*). Il *valore iImageID* è l'ID dell'elenco di immagini appropriato definito nel passaggio 2. Il *valore iIndex* è l'indice dell'immagine specifica all'interno dell'elenco.
4.  Aggiungere i pulsanti inviando al controllo della barra degli strumenti [**un \_ messaggio ADDBUTTONS**](tb-addbuttons.md) DA TB.

Il frammento di codice seguente illustra come aggiungere cinque pulsanti a una barra degli strumenti, con immagini di tre elenchi di immagini diversi. Il supporto per più elenchi di immagini è abilitato con un [**messaggio \_ CCM SETVERSION.**](ccm-setversion.md) Gli elenchi di immagini vengono quindi impostati e assegnati ID di 0-2. Ai pulsanti vengono assegnate immagini dagli elenchi di immagini come indicato di seguito:

-   Il pulsante 0 deriva dall'elenco immagini zero (ahim \[ 0 \] ) con indice 1.
-   Il pulsante 1 deriva dall'elenco immagini uno (ahim \[ 1 \] ) con indice 1.
-   Il pulsante 2 deriva dall'elenco di immagini due (ahim \[ 2 \] ) con indice 1.
-   Il pulsante 3 deriva dall'elenco immagini zero (ahim \[ 0 \] ) con indice 2.
-   Il pulsante 4 deriva dall'elenco immagini uno (ahim \[ 1 \] ) con indice 3.

Infine, i pulsanti vengono aggiunti al controllo barra degli strumenti con un [**messaggio \_ ADDBUTTONS DA**](tb-addbuttons.md) TB.


```
//Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 2, (LPARAM)ahiml[2]);

    // Create the five buttons
    TBBUTTON rgtb[5];
    
    //... initialize the TBBUTTON structures as usual ...
    
    //Assign images to each button
    rgtb[0].iBitmap = MAKELONG(1, 0);
    rgtb[1].iBitmap = MAKELONG(1, 1);
    rgtb[2].iBitmap = MAKELONG(1, 2);
    rgtb[3].iBitmap = MAKELONG(2, 0);
    rgtb[4].iBitmap = MAKELONG(3, 1);

    // Add the five buttons to the toolbar control
    SendMessage(hwndTB, TB_ADDBUTTONS, 5, (LPARAM)(&rgtb);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))
</dt> </dl>

 

