---
description: Oggetti di attivazione
ms.assetid: 767d5f1c-2b8d-43b6-916b-035129e93204
title: Oggetti di attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 401b4643e7e19c8cf0b7235218eaed2e355565fdb82a9d3756558e1f11991cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035599"
---
# <a name="activation-objects"></a>Oggetti di attivazione

Un *oggetto di attivazione* è un oggetto helper usato per creare un altro oggetto, un po' simile a un class factory. Gli oggetti di attivazione espongono [**l'interfaccia IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

Un oggetto di attivazione consente di posticipare la creazione dell'oggetto di destinazione, perché è possibile mantenere un [**puntatore IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) senza creare l'oggetto di destinazione. Anche gli oggetti di attivazione possono essere serializzati e quindi usati per creare l'oggetto di destinazione in un altro processo. Ad esempio, gli oggetti di attivazione vengono usati per effettuare il marshalling dei componenti della pipeline dal processo dell'applicazione al processo PMP (Protected Media Path). Gli oggetti di attivazione vengono usati anche da alcune funzioni di enumerazione che restituiscono un elenco **di puntatori IMFActivate.** Prima che l'applicazione crei l'oggetto di destinazione, può ottenere informazioni sull'oggetto esaminando gli attributi nell'oggetto di attivazione.

Per creare l'oggetto di destinazione da un oggetto di attivazione, chiamare il [**metodo IMFActivate::ActivateObject.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) Il chiamante deve chiamare [**IMFActivate::ShutdownObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject) quando viene eseguito usando l'oggetto creato. Spesso l'applicazione crea l'oggetto di attivazione e la sessione multimediale chiama **ActivateObject**. In tal caso, la sessione multimediale, non l'applicazione, deve chiamare **ShutdownObject**. In altre situazioni, l'applicazione riceve un [**puntatore IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) dalla sessione multimediale e l'applicazione chiama **ActivateObject** e **ShutdownObject**. Ad esempio, vedere [Come riprodurre file multimediali protetti.](how-to-play-protected-media-files.md)

Gli oggetti di attivazione possono avere attributi e [**l'interfaccia IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) eredita [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Alcuni oggetti di attivazione usano attributi per configurare l'oggetto creato. Gli attributi specifici supportati da ogni oggetto sono documentati nel riferimento per la funzione di creazione dell'oggetto di attivazione. Impostare gli attributi usando **il puntatore IMFActivate** ricevuto dalla funzione.

Per la riproduzione protetta, viene effettuato il marshalling degli oggetti di attivazione nel processo PMP. Per supportare il marshalling, un oggetto di attivazione deve esporre **l'interfaccia IPersistStream.** Inoltre, sia l'oggetto di attivazione che l'oggetto creato devono essere componenti attendibili se il PMP è in esecuzione in un processo protetto. Questo non è un requisito quando il PMP viene caricato in un processo non protetto.

Per usare un oggetto pipeline personalizzato, ad esempio un sink multimediale, all'interno del processo PMP, è necessario implementare un oggetto di attivazione per l'oggetto pipeline:

-   L'oggetto di attivazione deve esporre [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) e **IPersistStream**.
-   Il metodo **IPersist::GetClassID** dell'oggetto di attivazione deve restituire il CLSID dell'oggetto di attivazione.
-   Facoltativamente, è possibile implementare i metodi **IPersistStream::Save** e **IPersistStream::Load** per effettuare il marshalling di tutti i dati necessari per configurare l'oggetto di attivazione.

Quando la sessione multimediale carica la topologia all'interno del processo PMP, chiama **CoCreateInstance** per creare una nuova istanza dell'oggetto di attivazione. Chiama quindi [**IMFActivate::ActivateObject per**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) creare l'oggetto pipeline.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation API della piattaforma](media-foundation-platform-apis.md)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> </dl>

 

 



