---
title: Tipi di annotazione dinamica
description: Sono supportati tre tipi di annotazione dinamica in Microsoft Active Accessibility annotazione diretta, annotazione con mapping di valore e annotazione server. Ogni tipo offre vantaggi specifici, quindi è importante comprendere le differenze.
ms.assetid: 113fea65-982e-4291-9d60-bbb57282f3f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0453d3b5d05e2713d1a57fb0f475d4ec2a481b02
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856157"
---
# <a name="types-of-dynamic-annotation"></a>Tipi di annotazione dinamica

In Microsoft Active Accessibility sono supportati tre tipi di annotazione dinamica: annotazione *diretta*, *annotazione con mapping di valore* e *annotazione server*. Ogni tipo offre vantaggi specifici, quindi è importante comprendere le differenze.

## <a name="direct-annotation"></a>Annotazione diretta

L'annotazione diretta è la forma più semplice di annotazione dinamica. È più applicabile per gli elementi accessibili la cui proprietà annotata non dipende dallo stato del controllo e non richiede il supporto aggiuntivo fornito dall'annotazione con mapping di valore e dall'annotazione del server. L'annotazione diretta viene utilizzata per eseguire l'override del valore di una o più proprietà di Microsoft Active Accessibility di un elemento accessibile e per eseguire l'override o aggiungere una proprietà di automazione interfaccia utente Microsoft al controllo. Tutte le annotazioni apportate in una proprietà di Microsoft Active Accessibility vengono riflesse nella conversione di automazione interfaccia utente e nel proxy di automazione da Active Accessibility a interfaccia utente Microsoft. Per ulteriori informazioni, vedere [annotazione diretta](direct-annotation.md).

## <a name="value-map-annotation"></a>Annotazione mappa valori

Oltre a annotare direttamente le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , spesso è necessario convertire un valore specifico del controllo in una stringa che può essere riconosciuta da un utente finale. Un esempio è il controllo dispositivo di scorrimento risoluzione schermo nella scheda **Impostazioni** della finestra **proprietà di visualizzazione** (dal pannello di **controllo**). Mentre ogni posizione del dispositivo di scorrimento corrisponde a una risoluzione diversa (ad esempio, 640 x 480, 1024 x 768), il controllo non conosce la relazione e non può inviare tali informazioni a Microsoft Active Accessibility.

L'annotazione con mapping di valore rende più semplice questa attività. Utilizzando questa forma di annotazione, è possibile specificare le stringhe per i valori del dispositivo di scorrimento e specificare i ruoli, gli Stati e le descrizioni delle icone nelle visualizzazioni elenco ed albero. Per altre informazioni, vedere [annotazione della mappa dei valori](value-map-annotation.md).

## <a name="server-annotation"></a>Annotazione server

L'annotazione Server consente agli sviluppatori di registrare un oggetto callback per soddisfare le richieste client per la proprietà annotata di un elemento. Questo oggetto callback deve implementare l'interfaccia [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) ed essere registrato con i servizi di annotazione di Microsoft Active Accessibility. Al termine della registrazione, verrà chiesto di soddisfare tutte le richieste client per il valore della proprietà dell'elemento accessibile.

Una funzionalità particolarmente utile dell'annotazione del server è che un server può essere registrato una sola volta per gestire le richieste di un contenitore e di tutti i relativi elementi figlio. Quindi, ad esempio, un singolo server può essere configurato una sola volta per gestire le richieste per tutti gli elementi è una casella di riepilogo. Per altre informazioni, vedere [annotazione server](server-annotation.md).

 

 




