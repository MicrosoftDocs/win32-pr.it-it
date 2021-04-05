---
title: Come estendere lo schema
description: Quando le classi e/o gli attributi esistenti non rientrano nel tipo di dati che si desidera archiviare, potrebbe essere necessario estendere lo schema.
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- ANNUNCIO dello schema, come estendere
- Active Directory, utilizzo di, schema
- Active Directory, utilizzo di, schema, estensione dello schema, come estendere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437b23229182e6ec6f94b500feb764b4bbcf06e7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724495"
---
# <a name="how-to-extend-the-schema"></a>Come estendere lo schema

Quando le classi e/o gli attributi esistenti non rientrano nel tipo di dati che si desidera archiviare, potrebbe essere necessario estendere lo schema. Per ulteriori informazioni su come decidere quando estendere lo schema, vedere [estensione dello schema](extending-the-schema.md). Quando si è deciso che è richiesta l'estensione dello schema, utilizzare la procedura seguente per estendere lo schema.

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a>Verificare Active Directory funzionalità prima di applicare le estensioni dello schema

Verificare Active Directory funzionalità prima di aggiornare lo schema per garantire che l'estensione dello schema proceda senza errori. Assicurarsi almeno che tutti i controller di dominio per la foresta siano online ed eseguano la replica in ingresso.

**Per verificare Active Directory funzionalità prima di applicare l'estensione dello schema**

1.  Accedere a una workstation amministrativa in cui è installato lo strumento di supporto di Windows Repadmin.exe.
    > [!Note]  
    > Gli strumenti di supporto si trovano nel supporto di installazione del sistema operativo nella \\ cartella strumenti di supporto.

     

2.  Aprire un prompt dei comandi, quindi passare alla cartella in cui sono installati gli strumenti di supporto di Windows.
3.  Al prompt dei comandi digitare quanto segue e quindi premere INVIO:

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    Tutti i controller di dominio devono visualizzare 0 nella colonna errore e i Delta più grandi, che indicano il numero di modifiche apportate al database Active Directory dall'ultima replica completata, devono essere minori o approssimativamente uguali alla frequenza di replica del collegamento di sito utilizzato dal controller di dominio per la replica. La frequenza di replica predefinita è di 180 minuti.

    Per ulteriori informazioni sui passaggi aggiuntivi che è possibile eseguire per verificare Active Directory funzionalità prima di applicare l'estensione dello schema, vedere [l'articolo 325379 della Microsoft Knowledge base](https://support.microsoft.com/kb/325379/en-us).

**Per estendere lo schema**

1.  Determinare il metodo di estensione. Dopo aver progettato con attenzione le modifiche dello schema, il passaggio successivo consiste nel decidere quale metodo utilizzare per estendere lo schema. È possibile utilizzare uno dei metodi seguenti:
    -   Manualmente, usando i file di importazione. Vedere la documentazione [con lo strumento LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).
        > [!Note]  
        > Non usare LDIFDE per importare file Windows SCH \* . ldf. Tali file sono necessari per estendere lo schema di Active Directory per installare controller di dominio che eseguono una versione più recente di Windows Server rispetto alla versione in esecuzione nel master schema corrente. Quando è necessario estendere lo schema per poter installare un nuovo controller di dominio, utilizzare Adprep.exe.

         

    -   A livello di codice, usando un programma di installazione. Per ulteriori informazioni, vedere [estensione a livello di codice](programmatic-extension.md)
2.  Abilitare le modifiche dello schema. Per ulteriori informazioni, vedere [prerequisiti per l'installazione di un'estensione dello schema](prerequisites-for-installing-a-schema-extension.md) e [l'abilitazione delle modifiche dello schema nel master schema](enabling-schema-changes-at-the-schema-master.md).
3.  Ottenere un identificatore di oggetto (OID) per i nuovi attributi e/o le classi, come descritto in [ottenere un identificatore di oggetto](obtaining-an-object-identifier.md).
4.  Creare nuovi attributi e classi.
5.  Usare gli identificatori di visualizzazione per integrare nuovi attributi e classi con l'interfaccia utente, se necessario.
6.  Aggiornare la cache dello schema come descritto in [aggiornamento della cache dello schema](updating-the-schema-cache.md).
7.  Verificare l'estensione dello schema utilizzando LDP.exe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ottenere un identificatore di oggetto](obtaining-an-object-identifier.md)
</dt> <dt>

[Nuovi strumenti da riga di comando per Active Directory in Windows Server 2003](https://support.microsoft.com/kb/298882)
</dt> <dt>

[Utilizzo dello strumento LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))
</dt> <dt>

[Estensione dello schema di Active Directory](/previous-versions/ms806972(v=msdn.10))
</dt> <dt>

[Restrizioni sull'estensione dello schema](restrictions-on-schema-extension.md)
</dt> </dl>

 

 