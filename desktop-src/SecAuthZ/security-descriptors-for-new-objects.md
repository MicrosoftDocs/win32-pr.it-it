---
description: Quando si crea un oggetto a protezione diretta, è possibile assegnare un descrittore di sicurezza al nuovo oggetto.
ms.assetid: 5b276d27-31a4-4a83-83b0-c4044a427097
title: Descrittori di sicurezza per i nuovi oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3f9af674c83e4fc42448635bc54dfc0bb51b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308133"
---
# <a name="security-descriptors-for-new-objects"></a>Descrittori di sicurezza per i nuovi oggetti

Quando si crea un oggetto a protezione diretta, è possibile assegnare un [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) al nuovo oggetto. Le funzioni per la creazione di oggetti a protezione diretta, ad esempio [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa), hanno un parametro che punta alla struttura degli [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) che può contenere un puntatore al descrittore di sicurezza del nuovo oggetto. Per il codice di esempio che compila un descrittore di sicurezza e chiama **RegCreateKeyEx** per assegnare il descrittore di sicurezza a una nuova chiave del registro di sistema, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto in C++](creating-a-security-descriptor-for-a-new-object-in-c--.md)

Il componente o il server di sistema che gestisce l'oggetto può archiviare il descrittore di sicurezza specificato o predefinito per renderlo un attributo persistente dell'oggetto. Se il creatore di un oggetto non specifica un descrittore di sicurezza, il sistema utilizza le informazioni di sicurezza ereditate o predefinite per creare un descrittore di sicurezza. È possibile utilizzare le funzioni per modificare le informazioni nel descrittore di sicurezza di un oggetto.

Oggetti servizio directory, file, directory, chiavi del registro di sistema e desktop sono oggetti a protezione diretta che possono avere un oggetto padre. Quando si crea uno di questi oggetti, il sistema controlla le voci ACE ereditabili nel descrittore di sicurezza dell'oggetto padre. Il sistema unisce in genere qualsiasi ACE ereditabile negli ACL del descrittore di sicurezza del nuovo oggetto. È possibile impedire a un DACL o un SACL di ereditare le voci ACE impostando i bit protetti da SE \_ DACL \_ o se \_ SACL \_ protetti nei bit del controllo del descrittore di sicurezza. Per ulteriori informazioni, vedere [ereditarietà Ace](ace-inheritance.md).

 

 
