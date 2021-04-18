---
title: THEME. openDialog
description: Il metodo openDialog apre una finestra di dialogo file.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- THEME. openDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79b9478b6b970b1d8d18b6f40975479e4755fa6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333918"
---
# <a name="themeopendialog"></a>THEME. openDialog

Il metodo **openDialog** apre una finestra di dialogo file.

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*
</dt> <dd>

**Stringa** che specifica il tipo di finestra di dialogo. Deve essere impostato su "FILE \_ aperto".

</dd> <dt>

<span id="parameters"></span><span id="PARAMETERS"></span>*parametri*
</dt> <dd>

**Stringa** che può essere utilizzata per informazioni aggiuntive. Deve essere impostato su "FILES \_ ALLMEDIA".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce una **stringa** contenente l'URL del file selezionato o "" (stringa vuota) se l'utente fa clic su Annulla.

## <a name="remarks"></a>Commenti

Questo metodo può essere utilizzato per i file nei dischi rigidi locali o nelle unità di rete.

## <a name="examples"></a>Esempio


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
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

[**Elemento THEME**](theme-element.md)
</dt> </dl>

 

 





