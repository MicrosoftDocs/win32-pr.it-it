---
description: La DLL del filtro password di Windows, Passfilt.dll, viene eseguita nel contesto di sicurezza dell'account di sistema locale e consente di filtrare le password dell'account di dominio o locale.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Installazione e registrazione di una DLL di filtro password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd911c1a527384e48a2ae4567f6d85862e184cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882089"
---
# <a name="installing-and-registering-a-password-filter-dll"></a>Installazione e registrazione di una DLL di filtro password

È possibile utilizzare il filtro password di Windows per filtrare le password dell'account di dominio o locale. Per utilizzare il filtro password per gli account di dominio, installare e registrare la DLL in ogni controller di dominio nel dominio.

Per installare il filtro delle password, seguire questa procedura. È possibile eseguire questi passaggi manualmente oppure è possibile scrivere un programma di installazione per eseguire questi passaggi. Per eseguire questa procedura, è necessario essere un amministratore o appartenere al gruppo di amministratori.

**Per installare e registrare una DLL di filtro password Windows**

1.  Copiare la DLL nella directory di installazione di Windows nel controller di dominio o nel computer locale. Nelle installazioni standard, la cartella predefinita è \\ Windows \\ system32. Assicurarsi di creare una DLL di filtro password a 32 bit per computer a 32 bit e una DLL di filtro password a 64 bit per computer a 64 bit, quindi copiarli nel percorso appropriato.
2.  Per registrare il filtro password, aggiornare la seguente chiave del registro di sistema:

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    Se la sottochiave **pacchetti di notifica** esiste, aggiungere il nome della dll ai dati del valore esistente. Non sovrascrivere i valori esistenti e non includere l'estensione. dll.

    Se la sottochiave **pacchetti di notifica** non esiste, aggiungerla e quindi specificare il nome della dll per i dati del valore. Non includere l'estensione. dll.

    La sottochiave **pacchetti di notifica** può aggiungere più pacchetti.

3.  Individuare l'impostazione relativa alla complessità delle password.

    Nel pannello di controllo fare clic su **prestazioni e manutenzione**, fare clic su **strumenti di amministrazione**, fare doppio clic su **criteri di sicurezza locali**, fare doppio clic su criteri **account**, quindi fare doppio clic su **criteri password**.

4.  Per applicare sia il filtro password di Windows predefinito che il filtro password personalizzato, assicurarsi che l'impostazione dei criteri **password deve soddisfare i requisiti di complessità** sia abilitata. In caso contrario, disabilitare le **password devono soddisfare i requisiti di complessità** impostazione dei criteri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni sulla programmazione del filtro password](password-filter-programming-considerations.md)
</dt> <dt>

[Imposizione avanzata delle password e Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[Funzioni di filtro password](management-functions.md)
</dt> </dl>

 

 



