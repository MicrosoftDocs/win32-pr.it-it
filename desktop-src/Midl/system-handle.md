---
title: system_handle attributo
description: L'attributo \ system_handle\ specifica un tipo di handle definito dal sistema.
keywords:
- system_handle attributo MIDL
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1cc89818db201f1aca84aa63c6aa49b6b7d9f80b7b6c5e211e724004606c653e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641267"
---
# <a name="system_handle-attribute"></a>system_handle attributo

L system_handle attributo specifica un tipo di handle definito dal sistema \[  \] che rappresenta l'accesso a un oggetto di sistema.

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*system-handle-type* 
</dt> <dd>

Specifica una delle opzioni del tipo di handle di sistema.

Le opzioni valide sono:
* [sh_composition](sh-composition.md) : handle di superficie DirectComposition
* [sh_event:](sh-event.md) oggetto evento denominato o senza nome
* [sh_file:](sh-file.md) un file o un dispositivo di I/O
* [sh_job-](sh-job.md) Un oggetto processo
* [sh_mutex:](sh-mutex.md) oggetto mutex denominato o senza nome
* [sh_pipe-](sh-pipe.md) Un oggetto anonimo o named pipe
* [sh_process-](sh-process.md) Un oggetto processo
* [sh_reg_key-](sh-reg-key.md) Una chiave del Registro di sistema
* [sh_section](sh-section.md) - Sezione Della memoria condivisa
* [sh_semaphore:](sh-semaphore.md) oggetto semaforo denominato o senza nome
* [sh_socket-](sh-socket.md) Oggetto socket WinSock
* [sh_thread-](sh-thread.md) Oggetto thread
* [sh_token:](sh-token.md) oggetto token di accesso

</dd> <dt>

*optional-access-mask*
</dt> <dd>

Facoltativamente, richiede diritti di accesso specifici applicati all'handle duplicato. Per impostazione predefinita, quando non è specificato, l'handle verrà duplicato con lo stesso accesso. 

Per specificare un livello di accesso diverso, usare diritti di accesso specifici dell'oggetto corrispondenti all'oggetto di sistema sottostante selezionato.

Altre informazioni sulla propagazione dei diritti di accesso durante la duplicazione sono disponibili nella documentazione [di DuplicateHandle.](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

I collegamenti agli elenchi di diritti di accesso per ogni tipo di oggetto sono disponibili nel riferimento *DuplicateHandle* e nelle intestazioni **Vedere** anche di ogni `sh_*` pagina dei parametri.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare questo attributo, il flag deve essere impostato su (o versione successiva) quando si `-target` `NT100` esegue midl.exe.

Gli handle di sistema sono handle definiti dal sistema operativo per fornire l'accesso a una risorsa di sistema. Quando si dichiara l'attributo, è necessario specificare il tipo specifico dell'oggetto dietro l'handle.

Per un handle contrassegnato come , l'handle verrà duplicato nella procedura remota e `[in]` rimarrà valido per la durata di tale procedura. Al ritorno dalla procedura remota, l'handle duplicato viene liberato. Per mantenere l'accesso all'oggetto sottostante, l'applicazione remota deve duplicare l'handle nel proprio spazio indirizzi.

Al contrario, per un handle contrassegnato come , quando una procedura remota restituisce un handle da una chiamata, la procedura remota perde `[out]` la proprietà di esso. Per mantenere l'accesso all'oggetto sottostante, la procedura remota deve duplicare l'handle e restituire il duplicato. L'handle restituito diventa quindi di proprietà del chiamante che si assume la responsabilità di chiuderlo quando l'accesso all'oggetto di sistema sottostante non è più necessario.

Poiché si tratta di un meccanismo per l'inoltro dell'accesso a un oggetto di sistema, questo attributo è applicabile solo alle chiamate tra le procedure nello stesso computer.

I parametri di creazione e accesso forniti all'oggetto sottostante dietro l'handle di sistema al momento della creazione determinano se è possibile eseguire correttamente il marshalling nel contesto della procedura remota.

Una matrice di può essere passata in o out con la sintassi disponibile nella documentazione `system_handle` [**size_is'attributo.**](size-is.md)

## <a name="examples"></a>Esempio

Negli esempi seguenti vengono utilizzati diversi utilizzi di `system_handle` . Per un esempio completo, vedere [l'esempio SystemHandlePassing.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)

```c
interface MyInterface : IUnknown                         
{         
    HRESULT Proc1([in, system_handle(sh_file)] HANDLE writeThisFile);

    HRESULT Proc2([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE readThisPipe);

    HRESULT Proc3([out, system_handle(sh_composition)] HANDLE* visual);

    HRESULT Proc4([in] DWORD cEvents, [out, system_handle(sh_event), size_is(cEvents)] HANDLE* pWatchAllTheseEvents);
}
```

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
|-|-|
| Client minimo supportato | Windows 10 Aggiornamento dell'anniversario (versione 1607, build 14393) |
| Server minimo supportato | Windows Server 2016 (build 14393) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[Opzione /target](./-target.md)
</dt> <dt>

[Binding e handle](../Rpc/binding-and-handles.md)
</dt> <dt>

[Handle e oggetti](../sysinfo/handles-and-objects.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[Descrittori di sicurezza](../secauthz/security-descriptors.md)
</dt></dl>
