---
title: Tipi di utente sconosciuti
description: Tipi di utente sconosciuti
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4843ca2e19508806bba952403a2211a39f5a5ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339398"
---
# <a name="unknown-user-types"></a>Tipi di utente sconosciuti

È possibile semplificare la localizzazione dei prodotti aggiungendo la chiave del registro di sistema seguente:

**HKEY \_ \_Computer locali \\ software \\ Microsoft \\ OLE2** \\ **UnknownUserType**  =  *UserType*

Questa chiave consente alle funzioni di restituire una stringa specificata anziché un valore predefinito "Unknown", consentendo ai localizzatori di specificare un tipo di utente di una lingua diversa.

L'implementazione del gestore predefinito COM di [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) esamina il registro di sistema chiamando [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype). Se la classe dell'oggetto non viene trovata nel registro di sistema, viene restituito il tipo di utente dall'istanza [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) dell'oggetto. Se la classe non viene trovata nell'istanza di **IStorage** dell'oggetto, viene restituita la stringa "Unknown".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di applicazioni COM](registering-com-applications.md)
</dt> </dl>

 

 