---
description: Inviato alla funzione CPlApplet di un'applicazione del pannello di controllo per chiedere all'utente di eseguire l'inizializzazione globale, in particolare l'allocazione della memoria.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: Messaggio CPL_INIT (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f5206d773a7a0b1786b8c95104bbcf71561d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977354"
---
# <a name="cpl_init-message"></a>\_Messaggio init cpl

Inviato alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'applicazione del pannello di controllo per chiedere all'utente di eseguire l'inizializzazione globale, in particolare l'allocazione della memoria.


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'inizializzazione ha esito positivo, la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deve restituire un valore diverso da zero. In caso contrario, deve restituire zero.

Se [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) restituisce zero, l'applicazione di controllo termina la comunicazione e rilascia la DLL contenente l'applicazione del pannello di controllo.

## <a name="remarks"></a>Commenti

Poiché questo è l'unico modo in cui un'applicazione del pannello di controllo può segnalare una condizione di errore, l'applicazione deve allocare memoria in risposta a questo messaggio.

Questo messaggio viene inviato immediatamente dopo il caricamento della DLL che contiene l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
