---
title: Funzione di callback ReaderScroll
description: Funzione di callback definita dall'applicazione utilizzata quando il puntatore del mouse viene spostato all'interno della parte della finestra della modalità Reader dichiarata come area di scorrimento attiva.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- Controlli Windows per la funzione di callback ReaderScroll
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
ms.openlocfilehash: 0db5a80b84a30362e3bdbce45fe7485ad0dd6884
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964157"
---
# <a name="readerscroll-callback-function"></a>Funzione di callback ReaderScroll

\[*ReaderScroll* è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Funzione di callback definita dall'applicazione utilizzata quando il puntatore del mouse viene spostato all'interno della parte della finestra della modalità Reader dichiarata come area di scorrimento attiva.

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

*prmi* \[ in\]
</dt> <dd>

Tipo: **PREADERMODEINFO**

Puntatore alla struttura [**READERMODEINFO**](readermodeinfo.md) passata alla funzione [**DoReaderMode**](doreadermode.md) . Questa struttura definisce la finestra modalità lettore e l'area di scorrimento attiva.

</dd> <dt>

*dx* \[ in\]
</dt> <dd>

Tipo: **int**

Distanza per scorrere orizzontalmente. Se il \_ flag RMF VERTICALONLY è impostato nella struttura [**READERMODEINFO**](readermodeinfo.md) , questo valore è sempre 0.

</dd> <dt>

*dy* \[ in\]
</dt> <dd>

Tipo: **int**

Distanza di scorrimento verticale. Se il \_ flag RMF HORIZONTALONLY è impostato nella struttura [**READERMODEINFO**](readermodeinfo.md) , questo valore è sempre 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Questa funzione deve sempre restituire **true**.

## <a name="remarks"></a>Commenti

Quando l'applicazione riceve la notifica da questa funzione, l'applicazione è responsabile dello scorrimento della finestra modalità lettore nella direzione specificata dai parametri *dx* e *dy* .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata un'implementazione di questa funzione utilizzando una funzione personalizzata per eseguire lo scorrimento.


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
| Client minimo supportato<br/> | Windows Vista, \[ solo app desktop di Windows Vista\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>          |



 

