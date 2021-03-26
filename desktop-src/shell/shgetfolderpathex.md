---
UID: ''
title: SHGetFolderPathEx (funzione)
description: Recupera il percorso di una cartella nota identificata da KNOWNFOLDERID.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: SHGetFolderPath
ms.topic: reference
req.header: Shlobj.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Shell32.lib
req.dll: API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
api_name:
- SHGetFolderPathEx
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0dfc3342f3eca5622c25d2df7319cd2323f516ff
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2020
ms.locfileid: "104976575"
---
# <a name="shgetfolderpathex-function"></a>SHGetFolderPathEx (funzione)

## <a name="description"></a>Descrizione

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.
Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Recupera il percorso completo di una cartella nota identificata dal [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)della cartella.
Questo consente di estendere [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) consentendo di impostare la dimensione iniziale del buffer di stringa.

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a>Parametri

### <a name="rfid-in"></a>RFID [in]

Riferimento a **KNOWNFOLDERID** che identifica la cartella.

### <a name="dwflags-in"></a>dwFlags [in]

Flag che specificano opzioni di recupero speciali.
Questo valore può essere 0. in caso contrario, uno o più valori [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) .

### <a name="htoken-in-optional"></a>hToken [in, optional]

Un [token di accesso](/windows/desktop/SecAuthZ/access-tokens) che rappresenta un utente specifico.
Se questo parametro è **null**, ovvero l'utilizzo più comune, la funzione richiede la cartella nota per l'utente corrente.

Richiedere la cartella di un utente specifico passando il *hToken* dell'utente.
Questa operazione viene in genere eseguita nel contesto di un servizio con privilegi sufficienti per recuperare il token di un determinato utente.
Il token deve essere aperto con diritti [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) e [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) .
In alcuni casi, è necessario includere anche [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).
Oltre a passare il *hToken* dell'utente, è necessario montare l'hive del registro di sistema dell'utente specifico.
Per ulteriori informazioni sui problemi di controllo degli accessi, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control) .

Se si assegna il parametro *hToken* , il valore-1 indica l'utente predefinito.
Questo consente ai client di [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) di trovare i percorsi delle cartelle, ad esempio la cartella **Desktop** , per l'utente predefinito.
Il profilo utente predefinito viene duplicato quando viene creato un nuovo account utente e include cartelle speciali, ad esempio **documenti** e **Desktop**.
Tutti gli elementi aggiunti alla cartella utente predefinita vengono visualizzati anche in qualsiasi nuovo account utente.
Si noti che per l'accesso alle cartelle utente predefinite sono necessari i privilegi di amministratore.

### <a name="pszpath-out"></a>pszPath [out]

Stringa Unicode con terminazione null.
Il buffer deve essere di dimensioni cchPath.
Quando **SHGetFolderPathEx** viene restituito correttamente, questo parametro contiene il percorso della cartella nota.

### <a name="cchpath-in"></a>cchPath [in]

Dimensioni del buffer *ppszPath* , in caratteri.

## <a name="returns"></a>Restituisce

Restituisce **S_OK** in caso di esito positivo o un valore di errore.

## <a name="remarks"></a>Commenti

Poiché [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) è un wrapper per [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), questa funzione (**SHGetFolderPathEx**) funge anche da estensione per **SHGetFolderPath**.

## <a name="see-also"></a>Vedi anche

[KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)

[KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[SHGetKnownFolderIDList](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
