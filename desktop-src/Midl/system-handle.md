---
title: attributo system_handle
description: L'attributo \ system_handle \ specifica un tipo di handle definito dal sistema.
keywords:
- attributo system_handle MIDL
topic_type:
- apiref
api_name:
- system_handle
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f414654cdbd2eb07837455174f6142005f56a4b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320726"
---
# <a name="system_handle-attribute"></a>attributo system_handle

L' \[  \] attributo system_handle specifica un tipo di handle definito dal sistema che rappresenta l'accesso a un oggetto di sistema.

``` syntax
[system_handle(system-handle-type[,optional-access-mask])]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo di handle di sistema* 
</dt> <dd>

Specifica una delle opzioni del tipo di handle di sistema.

Le opzioni valide sono:
* [sh_composition](sh-composition.md) un handle di superficie DirectComposition
* [sh_event](sh-event.md) : oggetto evento denominato o senza nome
* [sh_file](sh-file.md) : un file o un dispositivo I/O
* [sh_job](sh-job.md) -un oggetto processo
* [sh_mutex](sh-mutex.md) : oggetto mutex denominato o senza nome
* [sh_pipe](sh-pipe.md) : oggetto anonimo o named pipe
* [sh_process](sh-process.md) un oggetto processo
* [sh_reg_key](sh-reg-key.md) -una chiave del registro di sistema
* [sh_section](sh-section.md) -una sezione di memoria condivisa
* [sh_semaphore](sh-semaphore.md) : oggetto semaforo denominato o senza nome
* [sh_socket](sh-socket.md) : oggetto socket Winsock
* [sh_thread](sh-thread.md) -oggetto thread
* [sh_token](sh-token.md) -un oggetto token di accesso

</dd> <dt>

*facoltativo-accesso-maschera*
</dt> <dd>

Facoltativamente, richiede diritti di accesso specifici applicati all'handle duplicato. Per impostazione predefinita, quando non è specificato, l'handle verrà duplicato con lo stesso accesso. 

Per specificare un livello di accesso diverso, usare i diritti di accesso specifici dell'oggetto corrispondenti all'oggetto di sistema sottostante selezionato.

Altre informazioni su come vengono propagati i diritti di accesso durante la duplicazione sono disponibili nella documentazione di [DuplicateHandle](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

I collegamenti agli elenchi di diritti di accesso per ogni tipo di oggetto sono reperibili nel riferimento *DuplicateHandle* , oltre che nella pagina **vedere anche** intestazioni di ogni `sh_*` parametro.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare questo attributo, il `-target` flag deve essere impostato su `NT100` (o versione successiva) quando si esegue midl.exe.

Gli handle di sistema sono handle definiti dal sistema operativo per fornire l'accesso a una risorsa di sistema. Quando si dichiara l'attributo, è necessario specificare il tipo specifico dell'oggetto sottostante all'handle.

Per un handle contrassegnato `[in]` , l'handle verrà duplicato nella procedura remota e rimarrà valido per la durata di tale procedura. Al ritorno dalla procedura remota, l'handle duplicato viene liberato. Per mantenere l'accesso all'oggetto sottostante, l'applicazione remota deve duplicare l'handle nello spazio degli indirizzi.

Al contrario, per un handle contrassegnato `[out]` , quando una procedura remota restituisce un handle da una chiamata, la procedura remota ne perderà la proprietà. Per mantenere l'accesso all'oggetto sottostante, la procedura remota deve duplicare l'handle e restituire il duplicato. L'handle restituito diventa quindi di proprietà del chiamante che presuppone che venga chiuso quando l'accesso all'oggetto di sistema sottostante non è più necessario.

Poiché si tratta di un meccanismo per inoltrare l'accesso a un oggetto di sistema, questo attributo è applicabile solo alle chiamate tra routine nello stesso computer.

I parametri di creazione e di accesso forniti all'oggetto sottostante dietro l'handle di sistema durante la creazione stabiliranno se è possibile eseguire correttamente il marshalling nel contesto della procedura remota.

Una matrice di `system_handle` può essere passata all'interno o all'esterno con la sintassi disponibile nella documentazione relativa all' [**attributo size_is**](size-is.md) .

## <a name="examples"></a>Esempio

Negli esempi seguenti vengono usati diversi usi di `system_handle` . Per un esempio completo, vedere l'esempio [SystemHandlePassing](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing) .

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
| Client minimo supportato | Aggiornamento dell'anniversario di Windows 10 (versione 1607, Build 14393) |
| Server minimo supportato | Windows Server 2016 (Build 14393) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>
<!--
[System Handle Passing sample code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/SystemHandlePassing)
</dt> <dt>
-->

[opzione/target](./-target.md)
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
