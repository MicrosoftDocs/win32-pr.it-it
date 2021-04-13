---
description: È possibile scrivere chiavi del registro di sistema nel registro di sistema dopo aver installato tutti i componenti selezionati e i file correlati.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Modifica del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6ff79ce340b0487c179cb37e44dff9f42e4be8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348526"
---
# <a name="modifying-the-registry"></a><span data-ttu-id="5822a-103">Modifica del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="5822a-103">Modifying the Registry</span></span>

<span data-ttu-id="5822a-104">È possibile scrivere chiavi del registro di sistema nel registro di sistema dopo aver installato tutti i componenti selezionati e i file correlati.</span><span class="sxs-lookup"><span data-stu-id="5822a-104">Registry keys can be written to the system registry once all selected components and their related files have been installed.</span></span> <span data-ttu-id="5822a-105">Le azioni standard relative alla modifica del registro di sistema devono essere sequenziate dopo le azioni standard di installazione dei file perché non è possibile scrivere chiavi del registro di sistema, a meno che il componente e il file corrispondenti non siano stati installati correttamente.</span><span class="sxs-lookup"><span data-stu-id="5822a-105">The standard actions related to modifying the registry must be sequenced after the file installation standard actions because registry keys cannot be written unless the corresponding component and file have been successfully installed.</span></span>

<span data-ttu-id="5822a-106">L' [azione RegisterClassInfo](registerclassinfo-action.md) accede alla [tabella della classe](class-table.md) per registrare le informazioni sulla classe com dei componenti installati.</span><span class="sxs-lookup"><span data-stu-id="5822a-106">The [RegisterClassInfo action](registerclassinfo-action.md) accesses the [Class table](class-table.md) to register the COM class information of the installed components.</span></span>

<span data-ttu-id="5822a-107">L' [azione RegisterExtensionInfo](registerextensioninfo-action.md) esegue una query sulla [tabella di estensione](extension-table.md) e sulla [tabella dei verbi](verb-table.md) e registra le estensioni corrispondenti e le informazioni sui verbi di comando con il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5822a-107">The [RegisterExtensionInfo action](registerextensioninfo-action.md) queries the [Extension table](extension-table.md) and [Verb table](verb-table.md) and registers the corresponding extensions and command-verb information with the operating system.</span></span>

<span data-ttu-id="5822a-108">L' [azione RegisterProgIdInfo](registerprogidinfo-action.md) gestisce la registrazione delle informazioni OLE ProgID con il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5822a-108">The [RegisterProgIdInfo action](registerprogidinfo-action.md) manages the registration of OLE ProgId information with the operating system.</span></span>

<span data-ttu-id="5822a-109">L' [azione RegisterMIMEInfo](registermimeinfo-action.md) elabora la [tabella MIME](mime-table.md) per registrare l'associazione tra un tipo di contesto MIME, l'estensione del nome del file e il CLSID.</span><span class="sxs-lookup"><span data-stu-id="5822a-109">The [RegisterMIMEInfo action](registermimeinfo-action.md) processes the [MIME table](mime-table.md) to register the association between a MIME context type, the file name extension, and the CLSID.</span></span>

<span data-ttu-id="5822a-110">L' [azione WriteRegistryValori consente](writeregistryvalues-action.md) elabora la [tabella del registro di sistema](registry-table.md) e scrive le chiavi per tutti i componenti installati localmente o per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="5822a-110">The [WriteRegistryValues action](writeregistryvalues-action.md) processes the [Registry table](registry-table.md) and writes the keys for all components that have been either installed locally or to run from source.</span></span> <span data-ttu-id="5822a-111">La tabella del registro di sistema consente di scrivere chiavi **nella \_ \_ radice delle classi HKEY**, **HKEY \_ \_ utente corrente**, **HKEY \_ \_ computer locale** e **HKEY \_ gli** hive del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5822a-111">The Registry table allows keys to be written to the **HKEY\_CLASSES\_ROOT**, **HKEY\_CURRENT\_USER**, **HKEY\_LOCAL\_MACHINE**, and **HKEY\_USERS** registry hives.</span></span>

<span data-ttu-id="5822a-112">L' [azione RemoveRegistryValues](removeregistryvalues-action.md) rimuove le chiavi contrassegnate per essere eliminate nella colonna Name della [tabella del registro di sistema](registry-table.md) o nella [tabella RemoveRegistry](removeregistry-table.md).</span><span class="sxs-lookup"><span data-stu-id="5822a-112">The [RemoveRegistryValues action](removeregistryvalues-action.md) removes the keys that have been marked to be deleted in the Name column of the [Registry table](registry-table.md) or the [RemoveRegistry Table](removeregistry-table.md).</span></span>

<span data-ttu-id="5822a-113">L' [azione RegisterTypeLibraries](registertypelibraries-action.md) elabora la [tabella TypeLib](typelib-table.md) e registra le librerie dei tipi installate nel sistema.</span><span class="sxs-lookup"><span data-stu-id="5822a-113">The [RegisterTypeLibraries action](registertypelibraries-action.md) processes the [TypeLib table](typelib-table.md) and registers the installed type libraries with the system.</span></span>

 

 



