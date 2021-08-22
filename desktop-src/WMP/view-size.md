---
title: VIEW.size
description: Il metodo size ridimensiona view su un bordo specificato.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- View.size Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0d9bd583b280f39bee38f0e109e6bb2bba6ce08ec0e7cea4c082b4a6db55739
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615311"
---
# <a name="viewsize"></a>VIEW.size

Il **metodo size** ridimensiona view **su** un bordo specificato.

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="handle"></span><span id="HANDLE"></span>*Gestire*
</dt> <dd>

Stringa che specifica il bordo o l'angolo da spostare durante il ridimensionamento. Questa stringa deve avere uno degli otto valori seguenti.



| Microsoft Edge   | Angolo      |
|--------|-------------|
| top    | Topright    |
| right  | in basso a destra |
| bottom | bottomleft  |
| sinistro   | Topleft     |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo viene in genere chiamato dall'interno di **un gestore onmousedown.** Si occupa del ridimensionamento mentre il mouse viene trascinato e interrompe il ridimensionamento quando viene rilasciato il pulsante del mouse. Se le dimensioni di **VIEW sono** limitate, non è possibile trascinare il mouse per ridimensionare **la vista** oltre i limiti limitati.

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
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> </dl>

 

 





