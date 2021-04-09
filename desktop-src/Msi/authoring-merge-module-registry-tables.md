---
description: Utilizzare le tabelle del registro di sistema del modulo merge in base al tipo di informazioni del registro di sistema.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Creazione di tabelle del registro di sistema del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10e31ac82d190c87019da5bc77408b58122a523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967267"
---
# <a name="authoring-merge-module-registry-tables"></a><span data-ttu-id="e4938-103">Creazione di tabelle del registro di sistema del modulo merge</span><span class="sxs-lookup"><span data-stu-id="e4938-103">Authoring Merge Module Registry Tables</span></span>

<span data-ttu-id="e4938-104">Utilizzare le tabelle del registro di sistema del modulo merge in base al tipo di informazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e4938-104">Use Merge Module Registry tables according to the type of registry information.</span></span>

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a><span data-ttu-id="e4938-105">TypeLib, Class, AppId, ProgId, estensione, verbo o tabelle MIME</span><span class="sxs-lookup"><span data-stu-id="e4938-105">TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME Tables</span></span>

<span data-ttu-id="e4938-106">Per le librerie dei tipi, le classi, le estensioni e i verbi, modificare le informazioni del registro di sistema nelle tabelle [typelib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md)o [MIME](mime-table.md) del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="e4938-106">For type libraries, classes, extensions, and verbs, author registry information into the merge module's [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="e4938-107">Se si utilizza la [tabella del registro](registry-table.md) di sistema per aggiungere queste informazioni, Windows 2000 non è in grado di fornire un annuncio a livello di sistema per questi componenti.</span><span class="sxs-lookup"><span data-stu-id="e4938-107">If you use the [Registry table](registry-table.md) to add this information, Windows 2000 cannot provide system-wide advertisement for these components.</span></span>

<span data-ttu-id="e4938-108">Gli autori dei moduli merge possono decidere di non eseguire la registrazione utilizzando la tabella delle classi per i motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e4938-108">Merge module authors may decide not to register using the Class table for the following reasons:</span></span>

-   <span data-ttu-id="e4938-109">Per essere registrato dalla tabella della classe, il file deve essere il percorso di base del relativo componente.</span><span class="sxs-lookup"><span data-stu-id="e4938-109">To be registered by the Class table, the file has to be the KeyPath of its component.</span></span> <span data-ttu-id="e4938-110">Questa operazione potrebbe richiedere una modifica inaccettabile nell'organizzazione dei componenti.</span><span class="sxs-lookup"><span data-stu-id="e4938-110">This may require an unacceptable change in the organization of components.</span></span>
-   <span data-ttu-id="e4938-111">Una chiamata COM può attivare il tentativo di reinstallare una classe annunciata da un programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="e4938-111">A COM call may trigger an installer attempt to reinstall an advertised class.</span></span> <span data-ttu-id="e4938-112">Gli autori possono decidere di non registrare una classe usando la tabella delle classi per evitare di attivare una reinstallazione quando il computer client non supporta un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="e4938-112">Authors may decide not to register a class using the Class table in order to avoid triggering a reinstallation when the client computer does not support a user interface.</span></span>

## <a name="registry-table"></a><span data-ttu-id="e4938-113">Tabella del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e4938-113">Registry Table</span></span>

<span data-ttu-id="e4938-114">Utilizzare la tabella del registro di sistema per aggiungere informazioni del registro di sistema che non possono essere create nelle tabelle TypeLib, Class, AppId, ProgId, Extension, verb o MIME.</span><span class="sxs-lookup"><span data-stu-id="e4938-114">Use the Registry table to add registry information that cannot be authored into the TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME tables.</span></span> <span data-ttu-id="e4938-115">Windows 2000 non può fornire un annuncio a livello di sistema per i componenti che usano la tabella del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e4938-115">Windows 2000 cannot provide system-wide advertisement for components that use the Registry table.</span></span>

<span data-ttu-id="e4938-116">Quando si crea la tabella del registro di sistema, fare riferimento ai percorsi dei file usando il \[ \# file \] o \[ . \]Formato di file anziché come \[ nome file della directory \] .</span><span class="sxs-lookup"><span data-stu-id="e4938-116">When authoring the Registry table, refer to file paths using the \[\#File\] or \[!File\] format rather than as \[Directory\]Filename.</span></span> <span data-ttu-id="e4938-117">Il secondo formato non supporta l'installazione dell'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="e4938-117">The latter format does not support run-from-source installation.</span></span> <span data-ttu-id="e4938-118">Il primo formato rende inoltre più semplice rilevare i file mancanti e i componenti difettosi.</span><span class="sxs-lookup"><span data-stu-id="e4938-118">The former format also makes missing files and faulty components easier to detect.</span></span>

<span data-ttu-id="e4938-119">È necessario prestare attenzione quando si utilizza il testo formattato nella colonna chiave della tabella del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e4938-119">Care is needed when using formatted text in the Key column of the Registry table.</span></span> <span data-ttu-id="e4938-120">Poiché Windows Installer non reinstalla i componenti già installati, l'utilizzo di testo formattato in questo campo può causare la rimozione delle chiavi del registro di sistema durante la rimozione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e4938-120">Because Windows Installer does not reinstall components that are already installed, using formatted text in this field may cause registry keys to be left behind on application removal.</span></span>

## <a name="selfreg-table"></a><span data-ttu-id="e4938-121">Tabella SelfReg</span><span class="sxs-lookup"><span data-stu-id="e4938-121">SelfReg Table</span></span>

<span data-ttu-id="e4938-122">Non è consigliabile usare la tabella SelfReg.</span><span class="sxs-lookup"><span data-stu-id="e4938-122">Using the SelfReg table is not recommended.</span></span> <span data-ttu-id="e4938-123">Per un elenco dei motivi per cui non si usa la registrazione automatica, vedere [tabella SelfReg](selfreg-table.md).</span><span class="sxs-lookup"><span data-stu-id="e4938-123">For a list of reasons for not using self-registration, see [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="e4938-124">È consigliabile utilizzare le tabelle TypeLib, Class, AppId, ProgId, Extension, verb e MIME, laddove possibile e la tabella del registro di sistema in tutti gli altri casi.</span><span class="sxs-lookup"><span data-stu-id="e4938-124">You should use the TypeLib, Class, AppId, ProgId, Extension, Verb, and MIME tables where possible instead and the Registry table in all other cases.</span></span>

 

 



