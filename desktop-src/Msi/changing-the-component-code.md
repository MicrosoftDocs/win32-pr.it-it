---
description: Quando si specificano i componenti per un'installazione, gli autori dei pacchetti devono seguire le regole generali per l'organizzazione dei componenti descritta in organizzazione di applicazioni in componenti.
ms.assetid: 7cf322e9-c49a-40a8-be4e-ab03ecba1c1f
title: Modifica del codice componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7531b4a38312d4abed038b612c4292c44af8e967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310995"
---
# <a name="changing-the-component-code"></a>Modifica del codice componente

Quando si specificano i [componenti](windows-installer-components.md) per un'installazione, gli autori dei pacchetti devono seguire le regole generali per l'organizzazione dei componenti descritta in [organizzazione di applicazioni in componenti](organizing-applications-into-components.md). È possibile che gli autori debbano introdurre nuovi componenti o modificare i componenti esistenti. Se l'aggiunta, la rimozione o la modifica delle risorse crea in modo efficace un nuovo componente, è necessario modificare anche il codice componente.

## <a name="creating-a-new-component"></a>Creazione di un nuovo componente

Introdurre un nuovo componente e assegnargli un codice componente univoco quando si apportano le modifiche seguenti:

-   Eventuali modifiche che non sono state visualizzate da test per essere compatibili con le versioni precedenti del componente. In questo caso, è necessario modificare anche il nome o il percorso di destinazione di ogni risorsa nel componente.
-   Una modifica del nome o del percorso di destinazione di qualsiasi file, chiave del registro di sistema, collegamento o altra risorsa nel componente. In questo caso, è necessario modificare anche il nome o il percorso di destinazione di ogni risorsa nel componente.
-   Aggiunta o rimozione di qualsiasi file, chiave del registro di sistema, collegamento o altra risorsa dal componente. In questo caso, è necessario modificare anche il nome o il percorso di destinazione di ogni risorsa nel componente.
-   Ricompilazione di un componente a 32 bit in un componente a 64 bit.

Quando si introduce un nuovo componente, gli autori devono eseguire una delle operazioni seguenti per assicurarsi che il componente non sia in conflitto con i componenti esistenti:

-   Modificare il nome o il percorso di destinazione di una risorsa che può essere installata con lo stesso nome e percorso di destinazione di un altro componente.
-   In caso contrario, garantire che il nuovo componente non venga mai installato nella stessa cartella di un altro componente con una risorsa con un nome e una posizione comuni. Sono incluse le versioni localizzate dei file con lo stesso nome file. Per ulteriori informazioni, vedere [cosa accade se le regole del componente sono interrotte?](what-happens-if-the-component-rules-are-broken.md).
-   Quando si modifica il codice componente di un componente esistente, modificare anche il nome o il percorso di destinazione di ogni file, chiave del registro di sistema, collegamento e altra risorsa nel componente.

### <a name="creating-a-new-version-of-a-component"></a>Creazione di una nuova versione di un componente

A una nuova versione di un componente viene assegnato lo stesso codice componente di un altro componente esistente. La modifica di un componente senza modificare il codice componente è facoltativa solo nei casi seguenti:

-   Le modifiche apportate al componente sono state collaudate in modo da garantire la compatibilità con le versioni precedenti del componente.
-   L'autore può garantire che la nuova versione del componente non venga mai installata in un sistema in cui si verificherebbe un conflitto con le versioni precedenti del componente o delle applicazioni che richiedono una versione precedente. Per ulteriori informazioni, vedere [cosa accade se le regole del componente sono interrotte?](what-happens-if-the-component-rules-are-broken.md).

Il codice componente di una nuova versione di un componente non deve essere modificato quando comporterebbe la condivisione di due componenti, ad esempio i valori del registro di sistema, i file o i collegamenti.

 

 



