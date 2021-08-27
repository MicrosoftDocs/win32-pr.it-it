---
title: Funzione di callback TranslateDispatch
description: Usato dal client della funzione DoReaderMode per intercettare e gestire in modo esplicito tutti i messaggi di windows destinati all'area di scorrimento della finestra in modalità lettore. Si tratta di una funzione di callback definita dall'applicazione.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- Funzione di callback TranslateDispatch Windows TranslateDispatch
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
ms.openlocfilehash: 08f726c3f56579260e96a882f1123d035df37cb3f7f71fd0ecbc47d41672359c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060531"
---
# <a name="translatedispatch-callback-function"></a>Funzione di callback TranslateDispatch

\[*TranslateDispatch* è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Usato dal client della funzione [**DoReaderMode**](doreadermode.md) per intercettare e gestire in modo esplicito tutti i messaggi di windows destinati all'area di scorrimento della finestra in modalità lettore. Si tratta di una funzione di callback definita dall'applicazione.

## <a name="syntax"></a>Sintassi


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpmsg* \[ Pollici\]
</dt> <dd>

Tipo: **const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) \***

Puntatore a una [**struttura MSG**](/windows/win32/api/winuser/ns-winuser-msg) che contiene il messaggio intercettato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE** se il messaggio è stato gestito da questa funzione. in caso contrario, **FALSE.** Se **FALSE,** il messaggio viene gestito dall'implementazione della modalità lettore predefinita. Tale implementazione gestisce lo spostamento del mouse e i pulsanti, nonché le pressione dei tasti.

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
| Client minimo supportato<br/> | Windows Vista, Windows solo \[ app desktop vista\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>          |



 

