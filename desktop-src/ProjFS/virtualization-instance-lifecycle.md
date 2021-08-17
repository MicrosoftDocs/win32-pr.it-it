---
title: Ciclo di vita dell'istanza di virtualizzazione
description: Panoramica del ciclo di vita di un'istanza di virtualizzazione ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: bbaaf5eca5481f3959e3e5afeb36a8cf6b264c939e8eb2cc9d84ba501d3c8530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792385"
---
# <a name="virtualization-instance-lifecycle"></a>Ciclo di vita dell'istanza di virtualizzazione

L'applicazione provider gestisce una o più istanze di virtualizzazione.  Ogni istanza di virtualizzazione passa attraverso quattro fasi del ciclo di vita:

1. Creazione
2. Avvio
3. Runtime
4. Arresta

Si noti che dopo l'arresto di un'istanza di virtualizzazione il provider non deve ri-crearla per riusarla.  Può semplicemente avviarlo di nuovo.

> **Nota:** questa sezione mostra esempi di API ProjFS.  Ogni esempio ha lo scopo di illustrare l'utilizzo delle API di base.  Per la documentazione delle opzioni non utilizzate in questi esempi, vedere le informazioni di [riferimento sull'API ProjFS.](/windows/desktop/api/_projfs)

## <a name="creating-a-virtualization-root"></a>Creazione di una radice di virtualizzazione

Prima che un provider possa avviare l'istanza di virtualizzazione che proietta gli elementi file system, deve creare la radice di virtualizzazione.  La radice di virtualizzazione è la directory in cui il provider proietta un albero di directory e file.

Per creare una radice di virtualizzazione, il provider deve:

1. Creare una directory da utilizzare come radice di virtualizzazione.

    Il provider crea una directory da usare come radice di virtualizzazione usando, ad esempio **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:

    ```C++
    HRESULT hr;
    const wchar_t* rootName = LR"(C:\virtRoot)";
    if (!CreateDirectoryW(rootName, nullptr))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        wprintf(L"Failed to create virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

1. Creare un ID istanza di virtualizzazione.

    Ogni istanza di virtualizzazione ha un ID univoco denominato _ID istanza di virtualizzazione_.  Il sistema usa questo valore per identificare a quale istanza di virtualizzazione è associato il contenuto.

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. Contrassegnare la nuova directory come radice di virtualizzazione.

    Il provider chiama **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** per contrassegnare la nuova directory come radice di virtualizzazione e assegnarla all'istanza di virtualizzazione.

    ```C++
    hr = PrjMarkDirectoryAsPlaceholder(rootName,
                                       nullptr,
                                       nullptr,
                                       &instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to mark virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

Il provider deve creare la radice di virtualizzazione una sola volta per ogni istanza di virtualizzazione.  Dopo aver creato una radice, l'istanza associata può essere avviata e arrestata ripetutamente senza ricreare la radice.

## <a name="starting-a-virtualization-instance"></a>Avvio di un'istanza di virtualizzazione

Dopo aver creato la radice di virtualizzazione, il provider deve avviare l'istanza di virtualizzazione.  Ciò segnala a ProjFS che il provider è pronto per ricevere callback e fornire dati.

Per avviare l'istanza di virtualizzazione, il provider deve:

1. Configurare la tabella di callback.

    ProjFS comunica con il provider richiamando le routine di callback implementate dal provider.  Il provider popola uno [struct PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) con puntatori alle routine di callback.

    ```C++
    PRJ_CALLBACKS callbackTable;

    // Supply required callbacks.
    callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
    callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
    callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
    callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
    callbackTable.GetFileDataCallback = MyGetFileDataCallback;

    // The rest of the callbacks are optional.
    callbackTable.QueryFileNameCallback = nullptr;
    callbackTable.NotificationCallback = nullptr;
    callbackTable.CancelCommandCallback = nullptr;
    ```

1. Avviare l'istanza di .

    Il provider chiama **[PrjStartVirtualizing per](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** avviare l'istanza di virtualizzazione.

    ```C++
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
    hr = PrjStartVirtualizing(rootName,
                              &callbackTable,
                              nullptr,
                              nullptr,
                              &instanceHandle);
    if (FAILED(hr))
    {
        wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
        return;
    }
    ```
    Il parametro _instanceHandle_ di **PrjStartVirtualizing** restituisce un handle all'istanza di virtualizzazione.  Il provider usa questo handle quando chiama altre API ProjFS.

## <a name="virtualization-instance-runtime"></a>Runtime dell'istanza di virtualizzazione

Al termine della chiamata a **PrjStartVirtualizing,** ProjFS richiama le routine di callback del provider in risposta alle file system nell'istanza di virtualizzazione.  Per informazioni su come il provider può gestire varie operazioni file system, vedere le sezioni seguenti:

* [Enumerazione di file e directory](enumerating-files-and-directories.md)
* [Fornire dati di file](providing-file-data.md)
* [Notifiche delle operazioni del file system](file-system-operation-notifications.md)
* [Gestione delle modifiche della visualizzazione](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a>Arresto di un'istanza di virtualizzazione

Per segnalare a ProjFS che il provider vuole interrompere la ricezione di callback e fornire dati, il provider deve arrestare l'istanza di virtualizzazione.  A tale scopo, il provider chiama **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, passando l'handle all'istanza di virtualizzazione ricevuta dalla chiamata a **PrjStartVirtualizing**.

```C++
PrjStopVirtualizing(instanceHandle);
```

Si noti che fino a quando questa chiamata non viene restituita, ProjFS può continuare a richiamare le routine di callback del provider.