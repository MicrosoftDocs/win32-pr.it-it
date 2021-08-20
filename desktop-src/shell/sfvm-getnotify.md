---
description: Notifica inviata all'oggetto callback di visualizzazione per specificare i percorsi e gli eventi da registrare per gli eventi di notifica delle modifiche.
title: SFVM_GETNOTIFY messaggio (Shlobj.h)
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
ms.openlocfilehash: 04c96793e329bfc18c6e6f01b4112429d76b58eabdec276d500c36677e58245c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677284"
---
# <a name="sfvm_getnotify-message"></a>Messaggio SFVM \_ GETNOTIFY

Notifica inviata all'oggetto callback di visualizzazione per specificare i percorsi e gli eventi da registrare per gli eventi di notifica delle modifiche. Dopo la registrazione, quando si verifica una modifica in in di questi percorsi o eventi, l'oggetto callback di visualizzazione viene notificato. Questi eventi vengono inviati al callback di visualizzazione [**tramite SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) e vengono quindi gestiti dalla vista.


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pidl* \[ Cambio\]
</dt> <dd>

Puntatore a un IDList assoluto di un elemento per il quale la visualizzazione deve registrare la notifica delle modifiche. In genere, è uguale a IDList della posizione visualizzata, ma può essere un'altra posizione.

> [!IMPORTANT]
> La durata di questo valore è di proprietà dell'oggetto callback di visualizzazione. È responsabilità dell'oggetto callback di visualizzazione creare e quindi liberare questo valore quando non è più necessario. Ciò richiede che l'oggetto callback di visualizzazione archivi questo valore. In genere, il valore può essere archiviato nel membro **\_ pidlMonitor** dell'oggetto callback di visualizzazione. Le regole di proprietà per il valore restituito tramite *pidl* sono non standard e richiedono particolare attenzione. L'oggetto callback di visualizzazione deve essere proprietario di questo valore e assicurarsi che non sia liberato fino a quando l'oggetto callback di visualizzazione stesso non viene eliminato.

 

</dd> <dt>

*lEvents* \[ Cambio\]
</dt> <dd>

Valore che contiene uno o più valori SHCNE. Per un elenco dei valori possibili, vedere [**SHChangeNotify.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) L'oggetto callback di visualizzazione verrà registrato per ricevere un [**messaggio SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) quando si verifica uno degli eventi associati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Ignorato, ma deve restituire S \_ OK.

## <a name="remarks"></a>Commenti

Se questo messaggio di callback non restituisce un valore diverso da zero per la maschera IDList o events, la visualizzazione non verrà registrato per le notifiche di modifica.

## <a name="examples"></a>Esempio

L'esempio seguente illustra un'implementazione di esempio del codice del gestore della funzione di callback di visualizzazione **per SFVM \_ GETNOTIFY**.


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
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SFVM \_ QUERYFSNOTIFY**](sfvm-queryfsnotify.md)
</dt> <dt>

[**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
