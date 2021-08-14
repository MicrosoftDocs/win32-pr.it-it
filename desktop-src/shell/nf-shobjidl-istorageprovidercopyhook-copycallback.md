---
description: Determina se la shell sarà autorizzata a spostare, copiare, eliminare o rinominare una cartella nella radice di sincronizzazione di un provider di servizi cloud.
title: IStorageProviderCopyHook::CopyCallback
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook::CopyCallback
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: 26fe9079e7fdf53809f8c0763fa38f271536f1339d16647936fb141f8d213be5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677979"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a>Metodo IStorageProviderCopyHook::CopyCallback

Determina se la shell sarà autorizzata a spostare, copiare, eliminare o rinominare una cartella nella radice di sincronizzazione di un provider di servizi cloud.

## <a name="syntax"></a>Sintassi

```C++
HRESULT CopyCallback( 
    HWND hwnd,
    UINT operation,
    UINT flags,
    LPCWSTR srcFile,
    DWORD srcAttribs,
    LPCWSTR destFile,
    DWORD destAttribs,
    UINT* result
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*hwnd* \[ Pollici\]
</dt> <dd>

Handle per la finestra che il gestore hook di copia deve usare come elemento padre per tutti gli elementi dell'interfaccia utente che il gestore deve visualizzare. Se **FOF_SILENT** specificato *nell'operazione*, il metodo deve ignorare questo parametro.

</dd> </dl>

<dl> <dt>

*operazione* \[ Pollici\]
</dt> <dd>

Operazione da eseguire. Questo parametro può essere uno dei valori elencati nel **membro wFunc** della [struttura SHFILEOPSTRUCT.](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa)

</dd> </dl>

<dl> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Flag che controllano l'operazione. Questo parametro può essere uno o più dei valori elencati nel *membro fFlags* della [struttura SHFILEOPSTRUCT.](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa)

Per gli hook di copia della stampante, questo valore è uno dei valori seguenti definiti in shellapi.h.

| Valore       | Descrizione |
|-------------|------------|
|  **PO_DELETE**      | È in corso l'eliminazione di una stampante. Il *parametro srcFile* punta al percorso completo della stampante specificata.           |
|  **PO_RENAME**       | È in corso la ridenominazione di una stampante. Il *parametro srcFile* punta al nuovo nome della stampante. Il *parametro destFile* punta al nome precedente.           |
| **PO_PORTCHANGE**    | Non supportata. Non usare.          |
| **PO_REN_PORT**    | Non supportata. Non usare.           |

</dd> </dl>

<dl> <dt>

*srcFile* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa che contiene il nome della cartella di origine.

</dd> </dl>

*srcAttribs* \[ Pollici\]
</dt> <dd>

Attributi della cartella di origine. Questo parametro può essere una combinazione di qualsiasi flag di attributo di file (FILE_ATTRIBUTE_*) definito nei file di intestazione. Vedere [Costanti di attributi di file.](../fileio/file-attribute-constants.md)

</dd> </dl>

*destFile* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa che contiene il nome della cartella di destinazione.

</dd> </dl>

*destAttribs* \[ Pollici\]
</dt> <dd>

Attributi della cartella di destinazione. Questo parametro può essere una combinazione di qualsiasi flag di attributo di file (FILE_ATTRIBUTE_*) definito nei file di intestazione. Vedere [Costanti di attributi di file.](../fileio/file-attribute-constants.md)

</dd> </dl>

*risultato* \[ Cambio\]
</dt> <dd>

Valore intero che indica se shell deve eseguire l'operazione. I tipi validi sono:

| Valore       | Descrizione |
|-------------|------------|
| **IDYES**       | Consente l'operazione.           |
| **IDNO**        | Impedisce l'operazione in questa cartella, ma continua con qualsiasi altra operazione che è stata approvata (ad esempio, un'operazione di copia batch).           |
| **IDCANCEL**    | Impedisce l'operazione corrente e annulla eventuali operazioni in sospeso.           |


</dd> </dl>


## <a name="return-value"></a>Valore restituito

Restituisce **S_OK** in caso di esito positivo oppure un codice di errore in caso contrario.

## <a name="remarks"></a>Commenti

La shell chiama il gestore dell'hook di copia del provider di servizi cloud per ogni cartella nella radice di sincronizzazione registrata. Per registrare un gestore hook di copia per le cartelle cloud, impostare il valore **CopyHook** nella chiave **HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Explorer/SyncRootManager/{SyncRootId}** sul CLSID dell'oggetto hook di copia.

Quando viene **chiamato il metodo CopyCallback,** la shell inizializza direttamente l'interfaccia [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) senza usare prima [un'interfaccia IShellExtInit.](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 10 Insider Preview Build 19624                                |
| Intestazione                   | shobjidl.h   |

## <a name="see-also"></a>Vedi anche

[Creare un motore di sincronizzazione cloud che supporta i file segnaposto](../cfapi/build-a-cloud-file-sync-engine.md)