---
description: Gli eventi WMI vengono recapitati dal provider di eventi a un consumer temporaneo o permanente. Il sistema di eventi WMI usa il confronto dei descrittori di sicurezza per gli eventi e i SID dell'account utente per controllare l'accesso agli eventi.
ms.assetid: 86eaeb5c-c27e-4794-88e2-e0ffbb885290
ms.tgt_platform: multiple
title: Protezione degli eventi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31280a4be25e358e28477bf6be060637f3f96bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226821"
---
# <a name="securing-wmi-events"></a>Protezione degli eventi WMI

Gli eventi WMI vengono recapitati dal [*provider di eventi*](gloss-e.md) a un consumer [*temporaneo*](gloss-t.md) o [*permanente*](gloss-p.md) . Il sistema di eventi WMI usa il confronto dei [*descrittori di sicurezza*](gloss-s.md) per gli eventi e i [*SID*](gloss-s.md) dell'account utente per controllare l'accesso agli eventi.

Gli eventi vengono recapitati sotto forma di istanza di una classe di evento, in genere, ma non necessariamente, derivati da un [**\_ \_ evento**](--event.md). WMI fornisce varie classi di evento generali nelle [classi di sistema WMI](wmi-system-classes.md), ad esempio [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md). I provider possono anche fornire le proprie classi di evento. Il [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) , ad esempio, dispone di classi di evento che segnalano la modifica di una chiave o di un valore del registro di sistema, ad esempio [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).

Negli argomenti seguenti vengono fornite informazioni sulla protezione del recapito di eventi per i provider e la ricezione di eventi in modo sicuro per gli script client e le applicazioni:

-   [Fornire eventi in modo sicuro](providing-events-securely.md)
-   [Ricezione di eventi in modo sicuro](receiving-events-securely.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> </dl>

 

 
