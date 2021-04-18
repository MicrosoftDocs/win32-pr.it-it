---
title: Messaggio TB_SETIMAGELIST (COMmctrl. h)
description: Imposta l'elenco di immagini utilizzato dalla barra degli strumenti per visualizzare i pulsanti che si trovano nello stato predefinito.
ms.assetid: 432ffdfc-bb63-4405-90da-9392910fdbb6
keywords:
- Controlli di Windows Message TB_SETIMAGELIST
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
ms.openlocfilehash: bb0b7ad631e8b56824ae65a2b262c5478611e75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302124"
---
# <a name="tb_setimagelist-message"></a>TB- \_ messaggio di DIimmagine

Imposta l'elenco di immagini utilizzato dalla barra degli strumenti per visualizzare i pulsanti che si trovano nello stato predefinito.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[Versione 5,80.](common-control-versions.md) Indice dell'elenco. Se si usa un solo elenco di immagini o una versione precedente dei controlli comuni, impostare *wParam* su zero. Per informazioni dettagliate sull'uso di più elenchi di immagini, vedere la sezione Osservazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elenco di immagini da impostare. Se questo parametro è **null**, non viene visualizzata alcuna immagine nei pulsanti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elenco di immagini precedentemente utilizzato per visualizzare i pulsanti nello stato predefinito oppure **null** se non è stato impostato in precedenza alcun elenco di immagini.

## <a name="remarks"></a>Commenti

> [!Note]  
> L'applicazione è responsabile di liberare l'elenco di immagini dopo che la barra degli strumenti è stata eliminata.

 

Il **messaggio \_** non può essere combinato con [**TB \_ ADDBITMAP**](tb-addbitmap.md). Non può essere usato anche con le barre degli strumenti create con [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), che chiama **TB \_ ADDBITMAP** internamente. Quando si crea una barra degli strumenti con **CreateToolbarEx** o si usa **TB \_ ADDBITMAP** per aggiungere immagini, la barra degli strumenti gestisce l'elenco di immagini internamente. Il tentativo di modificarlo con l'insieme di **\_ Immagini TB** presenta conseguenze imprevedibili.

Con la [versione 5,80](common-control-versions.md) o successive dei controlli comuni, le immagini dei pulsanti non devono provenire dallo stesso elenco di immagini. Per usare più elenchi di immagini per le immagini dei pulsanti della barra degli strumenti:

1.  Abilitare più elenchi di immagini inviando la barra degli strumenti controllare un messaggio di [**\_ versione CCM**](ccm-setversion.md) con *wParam* (il numero di versione) impostato su 5.
2.  Per ogni elenco di immagini da usare, inviare la barra degli strumenti per il controllo di un messaggio di sedicizzazione **TB \_** . Impostare *wParam* su un valore *wParam* definito dall'applicazione che verrà utilizzato per identificare l'elenco. Impostare *lParam* sull'handle HIMAGELIST dell'elenco.
3.  Per ogni pulsante, impostare il membro **iBitmap** della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) del pulsante su MAKELONG (*iIndex*, *iImageID*). Il valore *iImageID* è l'ID dell'elenco di immagini appropriato definito nel passaggio due. Il valore *iIndex* è l'indice dell'immagine particolare all'interno dell'elenco.
4.  Aggiungere i pulsanti inviando la barra degli strumenti per il controllo di un messaggio [**TB \_ ADDBUTTONS**](tb-addbuttons.md) .

Nel frammento di codice seguente viene illustrato come aggiungere cinque pulsanti a una barra degli strumenti, con immagini di tre diversi elenchi di immagini. Il supporto per più elenchi di immagini è abilitato con un messaggio di [**\_ versione CCM**](ccm-setversion.md) . Gli elenchi di immagini vengono quindi impostati e assegnati gli ID 0-2. Ai pulsanti vengono assegnate immagini dagli elenchi di immagini, come indicato di seguito:

-   Il pulsante 0 è compreso nell'elenco di immagini zero (Ahim \[ 0 \] ) con indice 1.
-   Il pulsante 1 è compreso nell'elenco di immagini uno (Ahim \[ 1 \] ) con indice 1.
-   Il pulsante 2 è da Image List Two (Ahim \[ 2 \] ) con indice 1.
-   Il pulsante 3 è da Image List zero (Ahim \[ 0 \] ) con indice 2.
-   Il pulsante 4 è compreso nell'elenco di immagini uno (Ahim \[ 1 \] ) con indice 3.

Infine, i pulsanti vengono aggiunti al controllo Toolbar con un messaggio [**TB \_ ADDBUTTONS**](tb-addbuttons.md) .


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))
</dt> </dl>

 

