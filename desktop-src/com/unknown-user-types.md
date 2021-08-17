---
title: Tipi di utente sconosciuti
description: Tipi di utente sconosciuti
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ce5ee88d36399187bab24ce51f0ef1c3c074182f98ce30ff6dc7d370992ffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129463"
---
# <a name="unknown-user-types"></a>Tipi di utente sconosciuti

È possibile semplificare la localizzazione del prodotto aggiungendo la chiave del Registro di sistema seguente:

**HKEY \_ LOCAL \_ MACHINES SOFTWARE Microsoft \\ \\ \\ OLE2** \\ **UnknownUserType**  =  *usertype*

Questa chiave consente alle funzioni di restituire una stringa specificata anziché un valore predefinito "Unknown", consentendo ai localizzatori di specificare un tipo di utente di una lingua diversa.

L'implementazione del gestore predefinito COM [**di IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) esamina il Registro di sistema chiamando [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype). Se la classe dell'oggetto non viene trovata nel Registro di sistema, viene restituito il tipo di utente dell'istanza [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) dell'oggetto. Se la classe non viene trovata nell'istanza **IStorage** dell'oggetto, viene restituita la stringa "Unknown".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di applicazioni COM](registering-com-applications.md)
</dt> </dl>

 

 