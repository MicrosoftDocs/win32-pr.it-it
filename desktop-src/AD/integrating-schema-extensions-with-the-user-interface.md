---
title: Integrazione di estensioni dello schema con l'interfaccia utente
description: Gli strumenti di amministrazione di Active Directory Domain Services utilizzano un'architettura comune per connettere l'interfaccia utente amministrativa allo schema di directory.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446c3b5150d66357206bd1eb139a391d2408ee9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297727"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a><span data-ttu-id="584c2-103">Integrazione di estensioni dello schema con l'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="584c2-103">Integrating Schema Extensions with the User Interface</span></span>

<span data-ttu-id="584c2-104">Gli strumenti di amministrazione di Active Directory Domain Services utilizzano un'architettura comune per connettere l'interfaccia utente amministrativa allo schema di directory.</span><span class="sxs-lookup"><span data-stu-id="584c2-104">The administration tools of Active Directory Domain Services use a common architecture for connecting the administrative user interface to the directory schema.</span></span> <span data-ttu-id="584c2-105">Il fulcro di questa architettura è la classe di oggetti **displaySpecifier** .</span><span class="sxs-lookup"><span data-stu-id="584c2-105">The centerpiece of this architecture is the **displaySpecifier** object class.</span></span> <span data-ttu-id="584c2-106">Gli identificatori di visualizzazione e il relativo utilizzo sono descritti in dettaglio in [estensione dell'interfaccia utente per gli oggetti directory](extending-the-user-interface-for-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="584c2-106">Display specifiers and their usage are described in detail in [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

<span data-ttu-id="584c2-107">Quando si crea una nuova classe creando una sottoclasse di una classe esistente, è possibile utilizzare l'interfaccia utente esistente per la superclasse copiando l'identificatore di visualizzazione della superclasse.</span><span class="sxs-lookup"><span data-stu-id="584c2-107">When you create a new class by subclassing an existing class, you can leverage the existing UI for the superclass by copying the superclass' display specifier.</span></span> <span data-ttu-id="584c2-108">Un modo semplice per copiare l'identificatore di visualizzazione per una classe consiste nell'esportarlo in un file LDIF utilizzando LDIFDE, modificare il nome distinto e il CN, quindi importare il file LDIF modificato.</span><span class="sxs-lookup"><span data-stu-id="584c2-108">An easy way to copy the display specifier for a class is to export it into an LDIF file using LDIFDE, edit the Distinguished name and CN, then import the modified LDIF file.</span></span> <span data-ttu-id="584c2-109">Se la sottoclasse ha attributi aggiuntivi, sarà necessario fornire altre pagine delle proprietà per supportare la modifica.</span><span class="sxs-lookup"><span data-stu-id="584c2-109">If the subclass has additional attributes, you will need to provide additional property pages to support editing.</span></span> <span data-ttu-id="584c2-110">Se la sottoclasse dispone di proprietà aggiuntive, è necessario fornire le pagine di estensione della finestra di dialogo di creazione perché l'interfaccia utente fornita dalla superclasse non ha modo di creare questi nuovi attributi.</span><span class="sxs-lookup"><span data-stu-id="584c2-110">If the subclass has additional must-have properties, you will need to provide Creation Dialog extension pages since the UI provided by the superclass has no way to create these new attributes.</span></span>

 

 




