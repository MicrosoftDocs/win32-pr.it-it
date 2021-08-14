---
title: Come estendere lo schema
description: Quando le classi e/o gli attributi esistenti non si adattano al tipo di dati da archiviare, è possibile estendere lo schema.
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- Schema AD , Come estendere
- Active Directory, uso, schema
- Active Directory, uso, schema, estensione dello schema, come estendere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc30f7292c1c1077cc4e44a9f022a430af87bc3efe876a5c197b3fe370d3b95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188159"
---
# <a name="how-to-extend-the-schema"></a>Come estendere lo schema

Quando le classi e/o gli attributi esistenti non si adattano al tipo di dati da archiviare, è possibile estendere lo schema. Per altre informazioni su come decidere quando estendere lo schema, vedere [Estensione dello schema](extending-the-schema.md). Dopo aver deciso che l'estensione dello schema è necessaria, usare la procedura seguente per estendere lo schema.

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a>Verificare la funzionalità di Active Directory prima di applicare le estensioni dello schema

Verificare la funzionalità di Active Directory prima di aggiornare lo schema per assicurarsi che l'estensione dello schema proceda senza errori. Assicurarsi almeno che tutti i controller di dominio per la foresta siano online e che esercitino la replica in ingresso.

**Per verificare la funzionalità di Active Directory prima di applicare l'estensione dello schema**

1.  Accedere a una workstation amministrativa in cui è installato Windows Support Tool Repadmin.exe.
    > [!Note]  
    > Gli strumenti di supporto si trovano nel supporto di installazione del sistema operativo nella cartella \\ Strumenti di supporto.

     

2.  Aprire un prompt dei comandi e quindi passare alla cartella in cui sono installati gli Windows di supporto.
3.  Al prompt dei comandi digitare quanto segue e quindi premere INVIO:

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    Tutti i controller di dominio devono visualizzare 0 nella colonna Errori e i delta più grandi (che indicano il numero di modifiche apportate al database di Active Directory dopo l'ultima replica riuscita) devono essere minori o approssimativamente uguali alla frequenza di replica del collegamento di sito usata dal controller di dominio per la replica. La frequenza di replica predefinita è di 180 minuti.

    Per altre informazioni sui passaggi aggiuntivi che è possibile eseguire per verificare la funzionalità di Active Directory prima di applicare [l'estensione](https://support.microsoft.com/kb/325379/en-us)dello schema, vedere l'articolo 325379 nella Microsoft Knowledge Base .

**Per estendere lo schema**

1.  Determinare il metodo di estensione. Dopo aver progettato attentamente le modifiche dello schema, il passaggio successivo consiste nel decidere quale metodo usare per estendere lo schema. È possibile usare uno dei metodi seguenti:
    -   Manualmente, usando i file di importazione. Vedere la documentazione [Relativa all'uso dello strumento LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).
        > [!Note]  
        > Non usare LDIFDE per importare Windows file con estensione ldf di \* Sch. Questi file sono necessari per estendere lo schema di Active Directory per installare controller di dominio che eseguono una versione più recente di Windows Server rispetto alla versione in esecuzione nel master schema corrente. Quando è necessario estendere lo schema per installare un nuovo controller di dominio, usare Adprep.exe.

         

    -   A livello di codice, usando un programma di installazione. Per altre informazioni, vedere [Estensione a livello di codice](programmatic-extension.md)
2.  Abilitare le modifiche dello schema. Per altre informazioni, vedere [Prerequisiti per l'installazione di un'estensione dello schema](prerequisites-for-installing-a-schema-extension.md) e abilitazione delle modifiche dello schema nel master [schema.](enabling-schema-changes-at-the-schema-master.md)
3.  Ottenere un identificatore di oggetto (OID) per i nuovi attributi e/o classi, come descritto in [Ottenere un identificatore di oggetto](obtaining-an-object-identifier.md).
4.  Creare nuovi attributi e classi.
5.  Usare gli identificatori di visualizzazione per integrare nuovi attributi e classi con l'interfaccia utente, se necessario.
6.  Aggiornare la cache dello schema come descritto in [Aggiornamento della cache dello schema](updating-the-schema-cache.md).
7.  Verificare l'estensione dello schema usando LDP.exe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Recupero di un identificatore di oggetto](obtaining-an-object-identifier.md)
</dt> <dt>

[Nuovi strumenti da riga di comando per Active Directory in Windows Server 2003](https://support.microsoft.com/kb/298882)
</dt> <dt>

[Uso dello strumento LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))
</dt> <dt>

[Estensione dello schema di Active Directory](/previous-versions/ms806972(v=msdn.10))
</dt> <dt>

[Restrizioni per l'estensione dello schema](restrictions-on-schema-extension.md)
</dt> </dl>

 

 