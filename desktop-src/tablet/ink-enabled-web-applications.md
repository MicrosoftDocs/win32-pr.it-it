---
description: L'esempio Ink Blog illustra diverse tecniche utili che possono essere usate nelle applicazioni Web abilitate per l'input penna.
ms.assetid: 4a5a453d-e3c1-40e6-b0eb-99009f0024dd
title: Ink-Enabled applicazioni Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8097bd55c34abbcb4469d74642e9dbc9a5f29e3b0b7110a76543fd40f5b1ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043492"
---
# <a name="ink-enabled-web-applications"></a>Ink-Enabled applicazioni Web

[L'esempio Ink Blog](ink-blog-web-sample.md) illustra diverse tecniche utili che possono essere usate nelle applicazioni Web abilitate per l'input penna. Ad esempio, verificare se il computer client è in grado di supportare i controlli abilitati per l'input penna, inviare dati di input penna a un server e visualizzare i dati dell'input penna in una pagina Web.

## <a name="testing-ink-enablement"></a>Test dell'abilitazione dell'input penna

Può essere utile verificare se il computer client può visualizzare controlli abilitati per l'input penna. In questo modo è possibile fare in modo che le pagine Webmostrano un controllo se il client è un Tablet PC o un altro controllo in caso non lo sia. Un modo per testare questa operazione è tentare di creare un oggetto, ad esempio [InkOverlay,](/previous-versions/ms833057(v=msdn.10))che può essere creato solo in un computer in cui è installato il sistema operativo Windows Vista, Windows XP Tablet PC Edition o Windows XP Tablet PC Edition Software Development Kit (SDK). Se si crea l'oggetto all'interno di un blocco try/catch e si intercetta qualsiasi eccezione generata (spesso viene generata un'eccezione [FileNotFoundException](/previous-versions/windows/) per indicare che non è possibile trovare l'assembly con questo controllo), è possibile rilevare se il computer client può supportare i controlli abilitati per l'input penna. Nell'esempio questo codice è disponibile nel costruttore della `InkArea` classe .

## <a name="submitting-ink-data"></a>Invio di dati input penna

Un modo semplice per inviare dati è prendere i dati dal controllo abilitato per l'input penna, trasferirlo in un modulo nascosto e quindi inviare il modulo. L'input penna può essere serializzato usando [il metodo Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) e quindi convertito in una stringa. Nell'esempio il form nascosto è definito in AddBlog.aspx e la serializzazione dell'input penna viene gestita in , dove l'input penna viene serializzato in `InkArea.SerializeInkData` un'immagine GIF. Si noti che potrebbe essere serializzato in modo analogo anche in altri formati, ad esempio il formato ISF (Ink Serialized Format).

## <a name="displaying-ink-data"></a>Visualizzazione dei dati input penna

Nell'esempio AddBlog.aspx.cs include un metodo denominato che recupera i dati inviati al server e `Page_Load` salva i dati in file. Genera quindi pagine Web nel server che contengono tag img che fanno riferimento ai file con le immagini GIF. A questo punto è necessario passare solo a tali pagine per visualizzare le immagini dell'input penna. Si noti che se l'input penna è stato serializzato con un formato diverso, ad esempio Ink Serialized Format (ISF), è necessario convertire l'input penna in un'immagine nel server per visualizzarlo nei client che non sono tablet.

I client Tablet PC possono caricare nuovamente l'input penna in un controllo abilitato per l'input penna e consentire all'utente di modificare l'input penna tramite ISF. Questo vale anche per l'input penna salvato usando il valore **Gif** dell'enumerazione [PersistenceFormat,](/previous-versions/ms827245(v=msdn.10)) perché i dati ISF sono contenuti nei metadati GIF.

 

 
