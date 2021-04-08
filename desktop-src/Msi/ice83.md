---
description: ICE83 convalida la tabella MsiAssembly.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ac38b4455875314c85fa08c1cfdc329e0cb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049903"
---
# <a name="ice83"></a><span data-ttu-id="87fb4-103">ICE83</span><span class="sxs-lookup"><span data-stu-id="87fb4-103">ICE83</span></span>

<span data-ttu-id="87fb4-104">ICE83 convalida la [tabella MsiAssembly](msiassembly-table.md).</span><span class="sxs-lookup"><span data-stu-id="87fb4-104">ICE83 validates the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="87fb4-105">Questa azione personalizzata ICE Invia un errore se il percorso della chiave per un componente contenente un assembly Win32 è impostato sul file manifesto.</span><span class="sxs-lookup"><span data-stu-id="87fb4-105">This ICE custom action posts an error if the key path for a component containing a Win32 assembly is set to the manifest file.</span></span> <span data-ttu-id="87fb4-106">In modo esplicito, l'errore viene inserito se il valore immesso nel campo del percorso della [tabella dei componenti](component-table.md) è uguale al valore immesso nel \_ campo del manifesto del file della tabella MsiAssembly.</span><span class="sxs-lookup"><span data-stu-id="87fb4-106">Explicitly the error is posted if the value entered in the KeyPath field of the [Component table](component-table.md) equals the value entered in the File\_Manifest field of the MsiAssembly table.</span></span> <span data-ttu-id="87fb4-107">Questa azione personalizzata ICE Invia un errore se esiste almeno un record nella tabella MsiAssembly e la [tabella InstallExecuteSequence](installexecutesequence-table.md) non contiene sia l'azione [MsiPublishAssemblies](msipublishassemblies-action.md) che l' [azione MsiUnpublishAssemblies](msiunpublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="87fb4-107">This ICE custom action posts an error if there is at least one record in the MsiAssembly table and the [InstallExecuteSequence table](installexecutesequence-table.md) does not contain both the [MsiPublishAssemblies Action](msipublishassemblies-action.md) and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

## <a name="result"></a><span data-ttu-id="87fb4-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="87fb4-108">Result</span></span>

<span data-ttu-id="87fb4-109">ICE83 invia i seguenti errori.</span><span class="sxs-lookup"><span data-stu-id="87fb4-109">ICE83 posts the following errors.</span></span>



| <span data-ttu-id="87fb4-110">Errore ICE83</span><span class="sxs-lookup"><span data-stu-id="87fb4-110">ICE83 error</span></span>                                                                                                   | <span data-ttu-id="87fb4-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87fb4-111">Description</span></span>                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87fb4-112">Il percorso della chiave per l'assembly SxS Win32 (componente \_ = \[ 1 \] ) non deve essere il file manifesto</span><span class="sxs-lookup"><span data-stu-id="87fb4-112">The key path for Win32 SXS Assembly (Component\_=\[1\]) SHOULD NOT be its manifest file</span></span>                       | <span data-ttu-id="87fb4-113">ICE83 Invia questo errore quando il campo del percorso di un assembly Win32 è impostato sul relativo file manifesto (componente. GetPath = = MsiAssembly. file \_ manifest).</span><span class="sxs-lookup"><span data-stu-id="87fb4-113">ICE83 posts this error when the KeyPath field for a Win32 Assembly is set to its manifest file (Component.KeyPath == MsiAssembly.File\_Manifest).</span></span> <span data-ttu-id="87fb4-114">\[1 \] è il percorso di un percorso della tabella Component</span><span class="sxs-lookup"><span data-stu-id="87fb4-114">\[1\] is KeyPath in Component table</span></span>                          |
| <span data-ttu-id="87fb4-115">Entrambe le azioni MsiPublishAssemblies e MsiUnpublishAssemblies devono essere presenti nella tabella InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="87fb4-115">Both MsiPublishAssemblies AND MsiUnpublishAssemblies actions MUST be present in InstallExecuteSequence table.</span></span> | <span data-ttu-id="87fb4-116">ICE83 Invia questo errore quando è presente almeno una voce nella tabella MsiAssembly, ma la tabella InstallExecuteSequence non contiene sia l'azione MsiAssemblyPublish che l'azione MsiAssemblyUnpublish.</span><span class="sxs-lookup"><span data-stu-id="87fb4-116">ICE83 posts this error when there is at least one entry in the MsiAssembly table but the InstallExecuteSequence table does not contain both the MsiAssemblyPublish action and the MsiAssemblyUnpublish action.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="87fb4-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87fb4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87fb4-118">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="87fb4-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



