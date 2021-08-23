---
description: Quando si specificano i componenti per un'installazione, gli autori di pacchetti devono seguire le regole generali per l'organizzazione dei componenti descritte in Organizzazione delle applicazioni in componenti.
ms.assetid: 7cf322e9-c49a-40a8-be4e-ab03ecba1c1f
title: Modifica del codice del componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96217dbcdbdc63d444f95d73dec657cf1a5ddef4ed80128c85b7752e1ec0f0d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520201"
---
# <a name="changing-the-component-code"></a>Modifica del codice del componente

Quando si specificano i [componenti per](windows-installer-components.md) un'installazione, gli autori di pacchetti devono seguire le regole generali per l'organizzazione dei componenti descritte in Organizzazione delle applicazioni [in componenti](organizing-applications-into-components.md). Gli autori potrebbero dover introdurre nuovi componenti o modificare i componenti esistenti. Se l'aggiunta, la rimozione o la modifica delle risorse crea in modo efficace un nuovo componente, è necessario modificare anche il codice del componente.

## <a name="creating-a-new-component"></a>Creazione di un nuovo componente

Introdurre un nuovo componente e assegnare a esso un codice componente univoco quando si apporta una delle modifiche seguenti:

-   Qualsiasi modifica non mostrata dal test per essere compatibile con le versioni precedenti del componente. In questo caso, è necessario modificare anche il nome o il percorso di destinazione di ogni risorsa nel componente.
-   Modifica del nome o del percorso di destinazione di qualsiasi file, chiave del Registro di sistema, collegamento o altra risorsa nel componente. In questo caso, è necessario modificare anche il nome o il percorso di destinazione di ogni risorsa nel componente.
-   Aggiunta o rimozione di qualsiasi file, chiave del Registro di sistema, collegamento o altra risorsa dal componente. In questo caso, è necessario modificare anche il nome o il percorso di destinazione di ogni risorsa nel componente.
-   Ricompilazione di un componente a 32 bit in un componente a 64 bit.

Quando si introduce un nuovo componente, gli autori devono eseguire una delle operazioni seguenti per assicurarsi che il componente non sia in conflitto con i componenti esistenti:

-   Modificare il nome o il percorso di destinazione di qualsiasi risorsa che può essere installata con lo stesso nome e lo stesso percorso di destinazione da un altro componente.
-   In caso contrario, garantire che il nuovo componente non sia mai installato nella stessa cartella di un altro componente che dispone di una risorsa con un nome e un percorso comuni. Sono incluse le versioni localizzate dei file con lo stesso nome file. Per altre informazioni, vedere [Cosa accade se le regole del componente vengono interrotte?](what-happens-if-the-component-rules-are-broken.md).
-   Quando si modifica il codice del componente di un componente esistente, modificare anche il nome o il percorso di destinazione di ogni file, chiave del Registro di sistema, collegamento e altra risorsa nel componente.

### <a name="creating-a-new-version-of-a-component"></a>Creazione di una nuova versione di un componente

A una nuova versione di un componente viene assegnato lo stesso codice del componente di un altro componente esistente. La modifica di un componente senza modificare il codice del componente è facoltativa solo nei casi seguenti:

-   Le modifiche apportate al componente sono state verificate verificando la compatibilità con le versioni precedenti del componente.
-   L'autore può garantire che la nuova versione del componente non verrà mai installata in un sistema in cui sarebbe in conflitto con le versioni precedenti del componente o delle applicazioni che richiedono una versione precedente. Per altre informazioni, vedere [Cosa accade se le regole del componente vengono interrotte?](what-happens-if-the-component-rules-are-broken.md).

Il codice del componente di una nuova versione di un componente non deve essere modificato quando comporterebbe la condivisione di risorse da parte di due componenti, ad esempio valori del Registro di sistema, file o collegamenti.

 

 



