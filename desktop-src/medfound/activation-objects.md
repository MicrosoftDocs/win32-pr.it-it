---
description: Oggetti attivazione
ms.assetid: 767d5f1c-2b8d-43b6-916b-035129e93204
title: Oggetti attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8741cbfa8bc3801a23b4976e60c0a3ad028b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129555"
---
# <a name="activation-objects"></a>Oggetti attivazione

Un *oggetto di attivazione* è un oggetto helper utilizzato per creare un altro oggetto, in modo simile a un class factory. Gli oggetti attivazione espongono l'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .

Un oggetto Activation consente di rinviare la creazione dell'oggetto di destinazione, in quanto è possibile utilizzare un puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) senza creare l'oggetto di destinazione. Gli oggetti attivazione possono anche essere serializzati e quindi usati per creare l'oggetto di destinazione in un altro processo. Gli oggetti attivazione, ad esempio, vengono utilizzati per effettuare il marshalling dei componenti della pipeline dal processo dell'applicazione al processo di supporto protetto (PMP). Gli oggetti attivazione vengono usati anche da alcune funzioni di enumerazione che restituiscono un elenco di puntatori **IMFActivate** . Prima che l'applicazione crei l'oggetto di destinazione, è possibile ottenere informazioni sull'oggetto esaminando gli attributi sull'oggetto attivazione.

Per creare l'oggetto di destinazione da un oggetto Activation, chiamare il metodo [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) . Il chiamante deve chiamare [**IMFActivate:: ShutdownObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject) al termine dell'utilizzo dell'oggetto creato. Spesso l'applicazione crea l'oggetto attivazione e la sessione multimediale chiama **ActivateObject**. In tal caso, la sessione multimediale, non l'applicazione, deve chiamare **ShutdownObject**. In altre situazioni, l'applicazione riceve un puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) dalla sessione multimediale e l'applicazione chiama **ActivateObject** e **ShutdownObject**. Vedere ad esempio [come riprodurre file multimediali protetti](how-to-play-protected-media-files.md).

Gli oggetti attivazione possono avere attributi e l'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) eredita l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Alcuni oggetti attivazione utilizzano attributi per configurare l'oggetto creato. Gli attributi specifici supportati da ogni oggetto sono documentati nel riferimento per la funzione di creazione dell'oggetto di attivazione. Impostare gli attributi utilizzando il puntatore **IMFActivate** ricevuto dalla funzione.

Per la riproduzione protetta, viene effettuato il marshalling degli oggetti attivazione al processo PMP. Per supportare il marshalling, un oggetto Activation deve esporre l'interfaccia **IPersistStream** . Inoltre, l'oggetto attivazione e l'oggetto creato devono essere componenti attendibili se il file PMP è in esecuzione in un processo protetto. Questo non è un requisito quando il PMP viene caricato in un processo non protetto.

Per usare un oggetto pipeline personalizzato, ad esempio un sink multimediale, all'interno del processo PMP, è necessario implementare un oggetto attivazione per l'oggetto della pipeline:

-   L'oggetto Activation deve esporre [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) e **IPersistStream**.
-   Il metodo **IPersist:: GetClassID** dell'oggetto Activation deve restituire il CLSID dell'oggetto di attivazione.
-   Facoltativamente, è possibile implementare i metodi **IPersistStream:: Save** e **IPersistStream:: Load** per effettuare il marshalling dei dati necessari per configurare l'oggetto di attivazione.

Quando la sessione multimediale carica la topologia all'interno del processo PMP, chiama **CoCreateInstance** per creare una nuova istanza dell'oggetto di attivazione. Chiama quindi [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) per creare l'oggetto pipeline.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API della piattaforma Media Foundation](media-foundation-platform-apis.md)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> </dl>

 

 



