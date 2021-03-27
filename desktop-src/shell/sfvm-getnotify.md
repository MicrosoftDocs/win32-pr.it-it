---
description: Notifica inviata all'oggetto di callback di visualizzazione per specificare i percorsi e gli eventi che devono essere registrati per gli eventi di notifica delle modifiche.
title: Messaggio SFVM_GETNOTIFY (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87933217-dfa9-4aaf-9630-fa2c302b18fa
api_name:
- SFVM_GETNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f766ee74463dd820c0b55d501d5002a3378a97b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232336"
---
# <a name="sfvm_getnotify-message"></a>\_Messaggio GETNOTIFY SFVM

Notifica inviata all'oggetto di callback di visualizzazione per specificare i percorsi e gli eventi che devono essere registrati per gli eventi di notifica delle modifiche. Una volta registrate, quando si verifica una modifica in in questi percorsi o eventi, viene inviata una notifica all'oggetto di callback della visualizzazione. Questi eventi vengono inviati al callback di visualizzazione tramite [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) e vengono quindi gestiti dalla vista.


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PIDL* \[ out\]
</dt> <dd>

Puntatore a un IDList assoluto di un elemento per il quale la visualizzazione deve essere registrata per ricevere una notifica delle modifiche. In genere, si tratta dello stesso IDList della posizione visualizzata, ma può trattarsi di un altro percorso.

> [!IMPORTANT]
> La durata di questo valore è di proprietà dell'oggetto di callback della visualizzazione. È responsabilità dell'oggetto View callback creare e quindi liberare questo valore quando non è più necessario. Per questo è necessario che l'oggetto View callback memorizzi questo valore. In genere, il valore può essere archiviato nel membro **\_ pidlMonitor** dell'oggetto View callback. Le regole di proprietà per il valore restituito tramite *PIDL* sono non standard e richiedono particolare attenzione. L'oggetto di callback della visualizzazione deve essere proprietario di questo valore e assicurarsi che non venga liberato fino a quando l'oggetto di callback della visualizzazione non viene eliminato definitivamente.

 

</dd> <dt>

*Levent* \[ out\]
</dt> <dd>

Valore che contiene uno o più valori SHCNE. Per un elenco dei valori possibili, vedere [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) . L'oggetto View callback viene registrato per ricevere un messaggio [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) quando si verifica uno degli eventi associati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Ignorato, ma deve restituire S \_ OK.

## <a name="remarks"></a>Commenti

Se il messaggio di callback non restituisce un valore diverso da zero per IDList o mask eventi, la vista non verrà registrata per le notifiche di modifica.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata un'implementazione di esempio del codice del gestore della funzione di callback View per **SFVM \_ GetNotify**.


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_QUERYFSNOTIFY SFVM**](sfvm-queryfsnotify.md)
</dt> <dt>

[**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
