---
title: Tipi di annotazione dinamica
description: Esistono tre tipi di annotazione dinamica supportati in Microsoft Active Accessibility annotazione diretta, annotazione mappata ai valori e annotazione server. Ogni tipo offre vantaggi specifici, quindi è importante comprendere le differenze.
ms.assetid: 113fea65-982e-4291-9d60-bbb57282f3f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58d30abe3d34fc61a9c85ebce0f6f6e38d51a43b70bef7d28f82adc4b476d74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570931"
---
# <a name="types-of-dynamic-annotation"></a>Tipi di annotazione dinamica

Esistono tre tipi di annotazione dinamica supportati in Microsoft Active Accessibility: *annotazione* diretta, annotazione *mappata* ai valori e *annotazione server*. Ogni tipo offre vantaggi specifici, quindi è importante comprendere le differenze.

## <a name="direct-annotation"></a>Annotazione diretta

L'annotazione diretta è la forma più semplice di Annotazione dinamica. È più applicabile per gli elementi accessibili la cui proprietà annotata non dipende dallo stato del controllo e non richiede il supporto aggiuntivo fornito dall'annotazione mappata al valore e dall'annotazione server. L'annotazione diretta viene usata per eseguire l'override del valore di una o più proprietà Microsoft Active Accessibility di un elemento accessibile e per eseguire l'override o aggiungere una proprietà microsoft Automazione interfaccia utente al controllo. Tutte le annotazioni effettuate in Microsoft Active Accessibility proprietà vengono riflesse nella conversione Automazione interfaccia utente e nel proxy Microsoft Active Accessibility da Automazione interfaccia utente.) Per altre informazioni, vedere [Annotazione diretta](direct-annotation.md).

## <a name="value-map-annotation"></a>Annotazione mappa valori

Oltre ad annotare direttamente le proprietà [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) spesso è necessario convertire un valore specifico del controllo in una stringa che può essere compresa da un utente finale. Un esempio è il dispositivo di scorrimento della  risoluzione dello schermo **nella** scheda Impostazioni nella finestra Proprietà dello schermo (da **Pannello di controllo**). Mentre ogni posizione del dispositivo di scorrimento corrisponde a una risoluzione diversa (ad esempio, 640 x 480, 1024 x 768), il controllo non ha conoscenza di questa relazione e non può trasmettere queste informazioni a Microsoft Active Accessibility.

L'annotazione mappata al valore semplifica questa attività. Usando questa forma di annotazione, è possibile specificare stringhe per i valori del dispositivo di scorrimento e specificare ruoli, stati e descrizioni per le icone nelle visualizzazioni elenco e albero. Per altre informazioni, vedere [Annotazione mappa valori](value-map-annotation.md).

## <a name="server-annotation"></a>Annotazione server

L'annotazione server consente agli sviluppatori di registrare un oggetto callback per le richieste client di servizio per la proprietà annotata di un elemento. Questo oggetto callback deve implementare [**l'interfaccia IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) ed essere registrato con Microsoft Active Accessibility di annotazione. Dopo la registrazione, verrà richiesto di eseguire tutte le richieste client per il valore della proprietà dell'elemento accessibile.

Una funzionalità particolarmente utile dell'annotazione server è che un server può essere registrato una sola volta per gestire le richieste per un contenitore e tutti i relativi elementi figlio. Ad esempio, un singolo server può essere configurato una sola volta per gestire le richieste per tutti gli elementi è una casella di riepilogo. Per altre informazioni, vedere [Annotazione server](server-annotation.md).

 

 




