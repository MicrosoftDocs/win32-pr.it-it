---
description: L'oggetto Address rappresenta un'entità che può effettuare o ricevere chiamate.
ms.assetid: ab6db262-f99e-4027-9525-7597fcf02e72
title: Oggetto Address
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ae91e70d6d8efb56321ca4619c6eb973799024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883258"
---
# <a name="address-object"></a>Oggetto Address

L'oggetto Address rappresenta un'entità che può effettuare o ricevere chiamate. Questo oggetto espone interfacce e metodi che consentono a un'applicazione di eseguire una serie di operazioni, ad esempio:

-   Individuare se un indirizzo specificato può supportare un determinato set di requisiti del tipo di supporto.
-   Enumera le chiamate attualmente associate all'indirizzo.
-   Creare o inviare le chiamate.
-   Ottiene il nome del provider di servizi associato.
-   Se esiste un provider di servizi multimediali, ottenere i puntatori di interfaccia che consentono la manipolazione dettagliata del terminale.
-   Ottenere e impostare altre informazioni, ad esempio se un messaggio è in attesa.

La maggior parte degli indirizzi è associata a un terminale, ma questo non è uniformemente il caso. Ad esempio, un TSP remoto che fornisce l'accesso alle apparecchiature in un server avrà un indirizzo nel computer locale, ma non un terminale. Un modem senza voce non dispone anche di un terminale associato al relativo indirizzo.

Se a un indirizzo non è associato un terminale, l'interfaccia [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) non viene esposta nell'oggetto.

Nell'esempio di codice di [selezione di un indirizzo](select-an-address.md) viene illustrato il processo di base per l'acquisizione di un puntatore all'oggetto Address.

Vedere [Address Object Interfaces](address-object-interfaces.md) per un elenco di tutte le interfacce associate all'oggetto Address.

 

 
