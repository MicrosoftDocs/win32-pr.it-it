---
title: Accesso alla libreria
description: Accesso alla libreria
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Windows Media Player, libreria
- Modello a oggetti di Windows Media Player, libreria
- modello a oggetti, libreria
- Windows Media Player Mobile, libreria per il modello a oggetti
- Controllo ActiveX di Windows Media Player, libreria per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, libreria per il modello a oggetti
- Controllo ActiveX, libreria per il modello a oggetti
- Windows Media Player Library, accesso
- libreria, accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1a8fcc34324775d968f6eab49003c28452f76c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329876"
---
# <a name="library-access"></a>Accesso alla libreria

Le proprietà e i metodi del modello a oggetti di Windows Media Player che accedono alla libreria richiedono l'accesso in sola lettura o in lettura/scrittura al database. La libreria contiene informazioni che alcuni utenti vogliono tenere privato e che devono essere accessibili o modificate solo con il loro consenso.

Per Windows Media Player 9 Series o versioni successive, è possibile determinare il livello di accesso a livello di codice. Per determinare il livello corrente di accesso concesso al codice, recuperare le *Impostazioni*. proprietà **mediaAccessRights** . Tale proprietà restituisce "None", "Read" o "full" (Read/Write). Per richiedere diritti di accesso specifici, chiamare le *Impostazioni*. metodo **requestMediaAccessRights** , passando un parametro che specifica il livello richiesto. Il metodo Visualizza un messaggio all'utente che descrive il livello di accesso richiesto e restituisce un valore **booleano** che indica se l'accesso è stato concesso.

Determinati diritti di accesso vengono concessi automaticamente in base alla posizione in cui il codice è in esecuzione rispetto al computer dell'utente.

-   Se la pagina Web o il programma si trova nel computer dell'utente, per impostazione predefinita vengono concessi i diritti di accesso completi.
-   Le pagine Web hanno accesso in lettura al *lettore*. **currentMedia**, *Player*. **currentPlaylist** e *supporti*. **sourceURL** quando la pagina Web si trova in un'area di sicurezza di Internet Explorer che è uguale o meno limitata rispetto all'area di sicurezza dell'elemento multimediale o della playlist.

    Le aree di sicurezza sono la zona **attendibile** (incluso il computer locale dell'utente), l'area **Intranet locale** , l'area **Internet** e la zona **limitata** .

    Ad esempio, una pagina Web dell'area **Intranet locale** dispone di diritti di accesso completi al *lettore*. **currentMedia** quando l'elemento multimediale corrispondente si trova nella Intranet locale o in Internet, ma è necessario richiedere i diritti di accesso per gli elementi multimediali presenti nel computer locale di un utente o in un sito Web nell'area **attendibile** .

È necessario testare l'applicazione basata su Web o basata su Windows in tutte le aree di sicurezza che possono verificarsi. L'applicazione deve essere progettata per gestire il rifiuto di una richiesta di accesso in modo corretto.

Le versioni del modello a oggetti di Windows Media Player precedenti alla serie Windows Media Player 9 non includono **mediaAccessRights** o **requestMediaAccessRights**. Queste versioni precedenti di Windows Media Player consentono all'utente di impostare i livelli di accesso utilizzando la finestra di dialogo **Opzioni** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> <dt>

[**Utilizzo della libreria**](working-with-the-library.md)
</dt> </dl>

 

 




