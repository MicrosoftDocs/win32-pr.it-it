---
description: Un'applicazione invia il \_ messaggio WM MDIMAXIMIZE a una finestra del client di interfaccia a documenti multipli (MDI) per ingrandire una finestra figlio MDI.
ms.assetid: 7c5e4157-13f6-40d7-a64a-076bd14aca0d
title: Messaggio WM_MDIMAXIMIZE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8372bcb25f35a52793292de4fd94a4a9dadafe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306663"
---
# <a name="wm_mdimaximize-message"></a>\_Messaggio MDIMAXIMIZE WM

Un'applicazione invia il messaggio **WM \_ MDIMAXIMIZE** a una finestra del client di interfaccia a documenti multipli (MDI) per ingrandire una finestra figlio MDI. Il sistema ridimensiona la finestra figlio per fare in modo che l'area client riempia la finestra del client. Il sistema posiziona l'icona del menu finestra della finestra figlio nella posizione più a destra della barra dei menu della finestra cornice e posiziona l'icona di ripristino della finestra figlio nella posizione più a sinistra. Il sistema aggiunge anche il testo della barra del titolo della finestra figlio a quello della finestra cornice.


```C++
#define WM_MDIMAXIMIZE                  0x0225
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra figlio MDI da ingrandire.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **zero**

Il valore restituito è sempre zero.

## <a name="remarks"></a>Commenti

Se una finestra client MDI riceve un messaggio che modifica l'attivazione delle finestre figlio mentre la finestra figlio MDI attualmente attiva è ingrandita, il sistema ripristina la finestra figlio attiva e ingrandisce la finestra figlio appena attivata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_MDIRESTORE WM**](wm-mdirestore.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




