---
title: Moniker asincroni e sincroni
description: Moniker asincroni e sincroni
ms.assetid: 79c7894d-956a-4c86-8806-2c6c7faa6034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c631c669d73796d1596f52ab2ec6e724829ea80e6873523c1e9bd4f8ad567f09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071111"
---
# <a name="asynchronous-and-synchronous-monikers"></a>Moniker asincroni e sincroni

Un client di un moniker OLE standard sincrono in genere crea e contiene un riferimento al moniker, nonché il contesto di associazione da usare durante l'associazione. I componenti coinvolti nell'uso dei moniker tradizionali sono illustrati nel diagramma seguente.

![Diagramma che mostra il client connesso al contesto di associazione o a qualsiasi moniker per l'oggetto fornito dal sistema.](images/1b29d6fe-f6e7-4eec-91e7-5043c09ca4dc.png)

I client in genere creano moniker standard chiamando funzioni come [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker), [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)o [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) oppure, poiché possono essere salvate nell'archiviazione permanente, [**tramite OleSaveToStream**](/windows/desktop/api/ole/nf-ole-olesavetostream) [**e OleLoadFromStream**](/windows/desktop/api/ole/nf-ole-oleloadfromstream). I moniker possono anche essere ottenuti da un oggetto contenitore chiamando il [**metodo IBindHost::CreateMoniker.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) I client creano contesti di associazione chiamando la [**funzione CreateBindCtx**](/windows/desktop/api/Objbase/nf-objbase-createbindctx) e quindi passano il contesto di associazione al moniker con chiamate a [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) o [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).

Come illustrato nel diagramma seguente, anche un client di un moniker asincrono crea e contiene un riferimento al moniker e al contesto di associazione da usare durante l'associazione.

![Diagramma che mostra le connessioni tra Client-Provided, Disertore fornito e Fornito dal sistema.](images/86872be9-bcbb-4ce8-b69a-38ae5bd7ba41.png)

Per ottenere un comportamento asincrono, il client implementa [**l'interfaccia IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) in un oggetto bind-status-callback e chiama la funzione [**RegisterBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) o [**la funzione CreateAsyncBindCtx**](/windows/desktop/api/Urlmon/nf-urlmon-createasyncbindctx) per registrare questa interfaccia con il contesto di associazione. Il moniker passa un puntatore alla relativa [**interfaccia IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) in una chiamata al [**metodo IBindStatusCallback::OnStartBinding.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)) Il client indica al moniker asincrono come vuole eseguire l'associazione al ritorno dalla chiamata del moniker al metodo [**IBindStatusCallback::GetBindInfo.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker asincroni](asynchronous-monikers.md)
</dt> </dl>

 

 