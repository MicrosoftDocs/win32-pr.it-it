---
title: Visualizza. size
description: Il metodo size ridimensiona la visualizzazione in un bordo specificato.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- VISUALIZZAZIONE. dimensioni di Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: def9b416dfe5eda052ef430b587fa1c6017b4e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325967"
---
# <a name="viewsize"></a>Visualizza. size

Il metodo **size ridimensiona** la **visualizzazione** in un bordo specificato.

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="handle"></span><span id="HANDLE"></span>*gestire*
</dt> <dd>

Stringa che specifica il bordo o l'angolo da spostare durante il ridimensionamento. Questa stringa deve avere uno degli otto valori seguenti.



| Microsoft Edge   | Angolo      |
|--------|-------------|
| top    | TopRight    |
| right  | BottomRight |
| bottom | BottomLeft  |
| sinistro   | TopLeft     |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo viene in genere chiamato dall'interno di un gestore **OnMouseDown** . Esegue il ridimensionamento quando il mouse viene trascinato e interrompe il ridimensionamento quando viene rilasciato il pulsante del mouse. Se le dimensioni della **vista** sono limitate, non è possibile trascinare il mouse per ridimensionare la **visualizzazione** oltre i limiti limitati.

## <a name="examples"></a>Esempio


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> </dl>

 

 





