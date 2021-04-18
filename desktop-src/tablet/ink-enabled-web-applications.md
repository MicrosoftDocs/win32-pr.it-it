---
description: L'esempio di Blog Ink illustra diverse tecniche utili che possono essere usate nelle applicazioni Web abilitate per l'input penna.
ms.assetid: 4a5a453d-e3c1-40e6-b0eb-99009f0024dd
title: Applicazioni Web Ink-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b14e368c1d2e97e35afa6d72a0fe082f304c5fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306748"
---
# <a name="ink-enabled-web-applications"></a>Applicazioni Web Ink-Enabled

L'esempio di [Blog Ink](ink-blog-web-sample.md) illustra diverse tecniche utili che possono essere usate nelle applicazioni Web abilitate per l'input penna. Questi includono: test se il computer client può supportare i controlli abilitati per l'input penna, inviare dati Ink a un server e visualizzare i dati Ink in una pagina Web.

## <a name="testing-ink-enablement"></a>Test dell'abilitazione dell'input penna

Può essere utile verificare se il computer client può visualizzare i controlli abilitati per l'input penna. In questo modo è possibile avere thewebpageshow un controllo se il client è un Tablet PC o uno diverso in caso contrario. Un modo per verificare questo problema consiste nel tentare di creare un oggetto, ad esempio un oggetto [InkOverlay](/previous-versions/ms833057(v=msdn.10)), che può essere creato solo in un computer in cui è installato il sistema operativo Windows Vista, Windows XP Tablet PC Edition o Windows XP Tablet PC Edition Software Development Kit (SDK). Se si crea l'oggetto all'interno di un blocco try/catch e si intercettano tutte le eccezioni generate (spesso viene generata un'eccezione [FileNotFoundException](/previous-versions/windows/) per indicare che l'assembly con questo controllo non è stato trovato), è possibile rilevare se il computer client può supportare i controlli abilitati per l'input penna. Nell'esempio, questo codice si trova nel costruttore della `InkArea` classe.

## <a name="submitting-ink-data"></a>Invio di dati Ink

Un modo semplice per inviare i dati consiste nel prendere i dati dal controllo abilitato per l'input penna, trasferirli in un modulo nascosto e quindi inviare il modulo. È possibile serializzare l'input penna usando il metodo [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) e quindi convertirlo in una stringa. Nell'esempio, il form nascosto viene definito in AddBlog. aspx e la serializzazione dell'input penna viene gestita in `InkArea.SerializeInkData` , in cui l'input penna viene serializzato in un'immagine gif. Si noti che può essere serializzato in modo analogo anche in altri formati, ad esempio il formato ISF (Ink Serialized Format).

## <a name="displaying-ink-data"></a>Visualizzazione di dati Ink

Nell'esempio AddBlog. aspx. cs dispone di un metodo denominato `Page_Load` che recupera i dati inviati al server e li salva in file. Genera quindi pagine Web nel server che contiene i tag img che fanno riferimento ai file con le immagini GIF. A questo punto è sufficiente passare a tali pagine per visualizzare le immagini dell'input penna. Si noti che se l'input penna è stato serializzato con un formato diverso, ad esempio il formato ISF (Ink Serialized Format), è necessario convertire l'input penna in un'immagine sul server per visualizzarlo nei client che non sono tablet.

I client Tablet PC possono caricare nuovamente l'input penna in un controllo abilitato per l'input penna e consentire all'utente di modificare l'input penna tramite ISF. Questo vale anche per l'input penna salvato usando il valore **gif** dell'enumerazione [PersistenceFormat](/previous-versions/ms827245(v=msdn.10)) , perché i dati ISF sono contenuti nei metadati gif.

 

 
