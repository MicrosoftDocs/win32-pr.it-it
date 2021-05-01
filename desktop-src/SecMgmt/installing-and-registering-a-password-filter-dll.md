---
description: La DLL di filtro delle password di Windows, Passfilt.dll, viene eseguita nel contesto di sicurezza dell'account di sistema locale e consente di filtrare le password dell'account di dominio o locale.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Installazione e registrazione di una DLL di filtro password
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2e9f93630dc6bdaa5dbcc7e665a6b1cebff0e
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327166"
---
# <a name="installing-and-registering-a-password-filter-dll"></a>Installazione e registrazione di una DLL di filtro password

È possibile usare il filtro password di Windows per filtrare le password di dominio o dell'account locale. Per usare il filtro password per gli account di dominio, installare e registrare la DLL in ogni controller di dominio nel dominio.

Per installare il filtro password, seguire questa procedura. È possibile eseguire questi passaggi manualmente oppure scrivere un programma di installazione per eseguire questi passaggi. Per eseguire questa procedura, è necessario essere un amministratore o appartenere al gruppo di amministratori.

**Per installare e registrare una DLL di filtro password di Windows**

1.  Copiare la DLL nella directory di installazione di Windows nel controller di dominio o nel computer locale. Nelle installazioni standard la cartella predefinita è \\ \\ Windows System32. Assicurarsi di creare una DLL di filtro password a 32 bit per i computer a 32 bit e una DLL di filtro password a 64 bit per i computer a 64 bit e quindi copiarle nel percorso appropriato.
2.  Per registrare il filtro password, aggiornare la chiave del Registro di sistema di sistema seguente:

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    Se il **valore pacchetti di** notifica di tipo *REG_MULTI_SZ* esistente, aggiungere il nome della DLL ai dati di valore esistenti. Non sovrascrivere i valori esistenti e non includere l'estensione dll.

    Se il **valore Pacchetti di** notifica non esiste, crearlo, assegnargli il tipo *REG_MULTI_SZ* e quindi specificare il nome della DLL per i dati del valore. Non includere l'estensione dll.

    Il **valore Pacchetti di** notifica può aggiungere più pacchetti.

3.  Trovare l'impostazione di complessità della password.

    In Pannello di controllo fare clic su Prestazioni e manutenzione **,** su Strumenti di amministrazione **,** fare doppio clic su Criteri di sicurezza locali **,** fare doppio clic su Criteri account **,** quindi fare doppio clic su **Criteri password**.

4.  Per applicare sia il filtro password predefinito di Windows che il filtro password personalizzato, assicurarsi che l'impostazione dei criteri Password **deve soddisfare** i requisiti di complessità sia abilitata. In caso contrario, disabilitare **l'impostazione dei** criteri Password che devono soddisfare i requisiti di complessità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni sulla programmazione del filtro password](password-filter-programming-considerations.md)
</dt> <dt>

[Imposizione delle password complessa e Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[Funzioni di filtro password](management-functions.md)
</dt> </dl>

 

 



