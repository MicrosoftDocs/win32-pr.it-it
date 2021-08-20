---
title: Funzione di callback ReaderScroll
description: Funzione di callback definita dall'applicazione utilizzata quando il puntatore del mouse viene spostato all'interno della parte della finestra in modalità lettore dichiarata come area di scorrimento attiva.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- Funzione di callback ReaderScroll Windows controlli
topic_type:
- apiref
api_name:
- ReaderScroll
- PFNREADERSCROLL
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 554530e556161b4128199cda0a1a9d791f4f0ed75e8915c311d8945445486ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169111"
---
# <a name="readerscroll-callback-function"></a>Funzione di callback ReaderScroll

\[*ReaderScroll* è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Funzione di callback definita dall'applicazione utilizzata quando il puntatore del mouse viene spostato all'interno della parte della finestra in modalità lettore dichiarata come area di scorrimento attiva.

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK ReaderScroll(
  _In_ PREADERMODEINFO prmi,
  _In_ int             dx,
  _In_ int             dy
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*prmi* \[ Pollici\]
</dt> <dd>

Tipo: **PREADERMODEINFO**

Puntatore alla [**struttura READERMODEINFO**](readermodeinfo.md) passata alla [**funzione DoReaderMode.**](doreadermode.md) Questa struttura definisce la finestra in modalità lettore e l'area di scorrimento attiva.

</dd> <dt>

*dx* \[ in\]
</dt> <dd>

Tipo: **int**

Distanza di scorrimento orizzontale. Se il flag RMF \_ VERTICALONLY è impostato nella [**struttura READERMODEINFO,**](readermodeinfo.md) questo valore è sempre 0.

</dd> <dt>

*dy* \[ Pollici\]
</dt> <dd>

Tipo: **int**

Distanza di scorrimento verticale. Se il flag RMF \_ HORIZONTALONLY è impostato nella [**struttura READERMODEINFO,**](readermodeinfo.md) questo valore è sempre 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

Questa funzione deve sempre restituire **TRUE.**

## <a name="remarks"></a>Commenti

Quando l'applicazione riceve una notifica da questa funzione, l'applicazione è responsabile dello scorrimento della finestra in modalità lettore nella direzione specificata dai *parametri dx* *e dy.*

## <a name="examples"></a>Esempio

L'esempio seguente illustra un'implementazione di questa funzione usando una funzione personalizzata per eseguire lo scorrimento.


```C++
BOOL CALLBACK
ReaderScrollCallback(PREADERMODEINFO prmi, int dx, int dy)
{
    if (prmi == NULL) 
        return FALSE;

    // Call custom ScrollWindow method to scroll the window
    ScrollWindow(prmi->hwnd, dx, dy);
    
    return TRUE;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows solo \[ app desktop Vista\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>          |



 

