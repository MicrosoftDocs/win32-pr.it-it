---
title: Creazione di un esempio Project
description: Creazione di un esempio Project
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Windows Media Player negozi online, creazione di progetti di esempio
- negozi online, creazione di progetti di esempio
- negozi online di tipo 2, creazione di progetti di esempio
- Windows Media Player negozi online, progetti di esempio
- negozi online, progetti di esempio
- negozi online di tipo 2, progetti di esempio
- Windows Media Player negozi online, creazione guidata progetto
- negozi online, creazione guidata progetto
- tipo 2 negozi online, creazione guidata progetto
- plug-in, creazione guidata progetto
- Windows Media Player plug-in, creazione guidata progetto
- creazione di progetti di esempio
- esempi,tipo 2 negozi online
- Creazione guidata progetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b58af81123e257a7f71ad4be00e44c671f8ca3fa6f61b3719cd02ae1f928b7ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579937"
---
# <a name="creating-a-sample-project"></a>Creazione di un esempio Project

Per creare un nuovo progetto usando la creazione guidata del progetto, seguire questa procedura:

1.  Aprire Microsoft Visual Studio.
2.  Scegliere **Nuovo** dal menu **File**, quindi fare clic su **Progetto**.
3.  Nella casella **Project tipi di** progetto scegliere Visual C++ **Progetti**.
4.  Nella casella **di** riepilogo Modelli scegliere creazione **guidata Windows Media Player Online Stores.**
5.  Digitare un nome e un percorso per il progetto.
6.  Fare **clic su OK** per avviare la creazione guidata del progetto.
7.  Selezionare **Tipo 2 (integrazione di base)** e fare clic su **Avanti.**
8.  Digitare il nome descrittivo e l'ID distributore del contenuto per il servizio. Digitare l'URL della pagina Web che rimuove il servizio dal computer dell'utente.
    > [!Note]  
    > Il valore specificato per l'ID del server di distribuzione del contenuto non deve contenere spazi. La procedura guidata rimuove tutti gli spazi dalla stringa specificata.

     

9.  Fare clic su **Finish** (Fine) per creare il progetto.

La procedura guidata genera automaticamente un nuovo progetto C++ che crea un plug-in del negozio online di tipo 2 che implementa le interfacce **IWMPSubscriptionService** e **IWMPSubscriptionService2.** Ogni volta che si esegue la procedura guidata viene creato lo stesso progetto, ma il componente creato durante la compilazione del progetto ha un ID classe univoco. Anche il nome del progetto, il nome descrittivo e l'ID distributore del contenuto possono essere diversi a seconda dei valori specificati durante l'esecuzione della procedura guidata. Il progetto di esempio registra il componente usando un nome di chiave corrispondente al valore specificato per il nome descrittivo.

L'esempio usa Active Template Library (ATL) per fornire implementazioni COM.

La procedura guidata crea automaticamente i file seguenti:

-   *ProjectName* dll.cpp. Implementa le esportazioni dll (Dynamic Link Library), ad esempio la funzione principale del punto di ingresso della DLL. Contiene anche la mappa oggetti ATL e la dichiarazione del modulo.
-   *ProjectName*.cpp. Contiene le implementazioni predefinite per i metodi delle interfacce IWMPSubscriptionService e IWMPSubscriptionService2. Contiene anche il codice per definire le finestre di dialogo aperte dall'esempio quando i metodi vengono chiamati Windows Media Player.
-   *NomeProgetto*.def. Dichiara le esportazioni dll.
-   StdAfx.cpp. Include intestazioni standard.
-   wmp.h. File Windows Media Player di intestazione.
-   wmpplug.h. Il Windows Media Player di intestazione del plug-in.
-   subscriptionservices.h. Il Windows Media Player di intestazione dei negozi online.
-   resource.h. Contiene definizioni di risorse.
-   **NomeProgetto**.h. Contiene le definizioni di classe per l'oggetto negozio online e le finestre di dialogo. Definisce l'ID classe dell'oggetto e la costante dell'ID del distributore di contenuti.
-   StdAfx.h. Include il sistema standard.
-   *ProjectName*.rc. File script di risorsa. Contiene le definizioni per le risorse e i controlli della finestra di dialogo. Questa è anche la posizione in cui è archiviata la tabella delle stringhe. La tabella delle stringhe contiene il nome del progetto e le costanti di stringa del nome descrittivo. In genere si lavora con questo file nell'editor Visual Studio risorse, non come testo normale.
-   *ProjectName*.rgs. File script del Registro di sistema. Questo file contiene le informazioni usate per aggiungere la classe del componente al Registro di sistema Windows Media Player individuarla. È possibile modificare il nome della chiave per il servizio in questo file.

> [!Note]  
> È necessario impostare l'indirizzo di base per la DLL 0x0F100000 per evitare conflitti con Windows Media Player.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Compilazione del plug-in per uno Store online di tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[**Interfaccia IWMPSubscriptionService**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**Interfaccia IWMPSubscriptionService2**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




