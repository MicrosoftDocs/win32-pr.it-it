---
title: Funzione di callback TranslateDispatch
description: Utilizzato dal client della funzione DoReaderMode per intercettare e gestire in modo esplicito tutti i messaggi di Windows di destinazione per l'area di scorrimento della finestra modalità lettore. Si tratta di una funzione di callback definita dall'applicazione.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- Controlli Windows per la funzione di callback TranslateDispatch
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1230ed1e65f8d739f9a0a05e4788eb919c45c4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964109"
---
# <a name="translatedispatch-callback-function"></a>Funzione di callback TranslateDispatch

\[*TranslateDispatch* è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Utilizzato dal client della funzione [**DoReaderMode**](doreadermode.md) per intercettare e gestire in modo esplicito tutti i messaggi di Windows di destinazione per l'area di scorrimento della finestra modalità lettore. Si tratta di una funzione di callback definita dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpMsg* \[ in\]
</dt> <dd>

Tipo: **const [**msg**](/windows/win32/api/winuser/ns-winuser-msg) \** _

Puntatore a una struttura [_ *msg* *](/windows/win32/api/winuser/ns-winuser-msg) che contiene il messaggio intercettato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

**True** se il messaggio è stato gestito da questa funzione; in caso contrario, **false**. Se **false**, il messaggio viene gestito dall'implementazione della modalità Reader predefinita. Tale implementazione gestisce lo spostamento e i pulsanti del mouse, nonché le pressioni dei tasti.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata un'implementazione di questa funzione.


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, \[ solo app desktop di Windows Vista\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>          |



 

