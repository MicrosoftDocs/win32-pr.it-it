---
description: Determina se la shell sarà autorizzata a spostare, copiare, eliminare o rinominare una cartella nella radice di sincronizzazione di un provider cloud.
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
ms.openlocfilehash: c7df9296f2261e3907702067ca36265095102f34
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104995237"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a>Metodo IStorageProviderCopyHook:: CopyCallback

Determina se la shell sarà autorizzata a spostare, copiare, eliminare o rinominare una cartella nella radice di sincronizzazione di un provider cloud.

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

*HWND* \[ in\]
</dt> <dd>

Handle per la finestra che deve essere utilizzato dal gestore dell'hook di copia come elemento padre per gli elementi dell'interfaccia utente che possono essere visualizzati dal gestore. Se **FOF_SILENT** è specificato nell' *operazione*, il metodo deve ignorare questo parametro.

</dd> </dl>

<dl> <dt>

*operazione* \[ di in\]
</dt> <dd>

Operazione da eseguire. Questo parametro può essere uno dei valori elencati sotto il membro **wFunc** della struttura [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) .

</dd> </dl>

<dl> <dt>

*flag* \[ in\]
</dt> <dd>

Flag che controllano l'operazione. Questo parametro può essere uno o più dei valori elencati sotto il membro *fFlags* della struttura [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) .

Per gli hook di copia della stampante, questo valore corrisponde a uno dei valori seguenti definiti in Shellapi. h.

| Valore       | Descrizione |
|-------------|------------|
|  **PO_DELETE**      | È in corso l'eliminazione di una stampante. Il parametro *SrcFile* punta al percorso completo della stampante specificata.           |
|  **PO_RENAME**       | È in corso la ridenominazione di una stampante. Il parametro *SrcFile* punta al nuovo nome della stampante. Il parametro *destFile* punta al nome precedente.           |
| **PO_PORTCHANGE**    | Non supportata. Non usare.          |
| **PO_REN_PORT**    | Non supportata. Non usare.           |

</dd> </dl>

<dl> <dt>

*SrcFile* \[ in\]
</dt> <dd>

Puntatore a una stringa che contiene il nome della cartella di origine.

</dd> </dl>

*srcAttribs* \[ in\]
</dt> <dd>

Attributi della cartella di origine. Questo parametro può essere una combinazione di qualsiasi flag di attributo file (FILE_ATTRIBUTE_ *) definito nei file di intestazione. Vedere [costanti degli attributi di file](../fileio/file-attribute-constants.md).

</dd> </dl>

*destFile* \[ in\]
</dt> <dd>

Puntatore a una stringa che contiene il nome della cartella di destinazione.

</dd> </dl>

*destAttribs* \[ in\]
</dt> <dd>

Attributi della cartella di destinazione. Questo parametro può essere una combinazione di qualsiasi flag di attributo file (FILE_ATTRIBUTE_ *) definito nei file di intestazione. Vedere [costanti degli attributi di file](../fileio/file-attribute-constants.md).

</dd> </dl>

*risultato* \[ out\]
</dt> <dd>

Valore intero che indica se la shell deve eseguire l'operazione. I tipi validi sono:

| Valore       | Descrizione |
|-------------|------------|
| **IDYES**       | Consente l'operazione.           |
| **IDNO**        | Impedisce l'operazione su questa cartella ma continua con altre operazioni approvate, ad esempio un'operazione di copia batch.           |
| **IDCANCEL**    | Impedisce l'operazione corrente e Annulla tutte le operazioni in sospeso.           |


</dd> </dl>


## <a name="return-value"></a>Valore restituito

Restituisce **S_OK** in caso di esito positivo o un codice di errore.

## <a name="remarks"></a>Commenti

La shell chiama il gestore di hook di copia del provider cloud per ogni cartella sotto la radice di sincronizzazione registrata. Per registrare un gestore di hook di copia per le cartelle Cloud, impostare il valore **CopyHook** nella chiave **HKEY_LOCAL_MACHINE/software/Microsoft/Windows/CurrentVersion/Explorer/syncrootmanager/{syncrootid}** sul CLSID dell'oggetto copia hook.

Quando viene chiamato il metodo **CopyCallback** , la shell Inizializza direttamente l'interfaccia [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) senza usare prima un'interfaccia [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 10 Insider Preview Build 19624                                |
| Intestazione                   | ShObjIdl. h   |

## <a name="see-also"></a>Vedi anche

[Creare un motore di sincronizzazione cloud che supporti i file segnaposto](../cfapi/build-a-cloud-file-sync-engine.md)