---
title: Personalizzazione del plug-in dell'interfaccia utente
description: Personalizzazione del plug-in dell'interfaccia utente
ms.assetid: d961ed18-ba14-45af-90d3-b1e38dc53180
keywords:
- Plug-in di Windows Media Player, personalizzazione
- plug-in, personalizzazione
- plug-in dell'interfaccia utente, personalizzazione
- Plug-in dell'interfaccia utente, personalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4572c4ce5102443c3100ddd20719fe17fe62ffc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045123"
---
# <a name="customizing-the-ui-plug-in"></a><span data-ttu-id="86fdc-107">Personalizzazione del plug-in dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="86fdc-107">Customizing the UI Plug-in</span></span>

<span data-ttu-id="86fdc-108">A questo punto, il progetto è pronto per la personalizzazione.</span><span class="sxs-lookup"><span data-stu-id="86fdc-108">At this point, your project is ready for customization.</span></span> <span data-ttu-id="86fdc-109">È possibile modificare l'implementazione generata dalla procedura guidata dell'interfaccia **IWMPPluginUI** , è possibile aggiungere un'interfaccia utente alla classe **CPluginWindow** ed è possibile implementare una pagina delle proprietà nella classe **CPropertyDialog** .</span><span class="sxs-lookup"><span data-stu-id="86fdc-109">You can modify the wizard-generated implementation of the **IWMPPluginUI** interface, you can add a user interface to the **CPluginWindow** class, and you can implement a property page in the **CPropertyDialog** class.</span></span> <span data-ttu-id="86fdc-110">Se il plug-in è configurato per l'ascolto di eventi di Windows Media Player, la procedura guidata avrà generato implementazioni predefinite o vuote di tutti i gestori eventi necessari, che è possibile modificare o creare.</span><span class="sxs-lookup"><span data-stu-id="86fdc-110">If your plug-in is configured to listen to Windows Media Player events, the wizard will have generated default or empty implementations of all the necessary event handlers, which you also modify or create.</span></span>

<span data-ttu-id="86fdc-111">Il tipo di plug-in e le funzionalità supportate sono indicati da un valore archiviato nel registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="86fdc-111">The type of plug-in and the features it supports are indicated by a value which is stored in the Windows registry.</span></span> <span data-ttu-id="86fdc-112">La procedura guidata genera un file con estensione rgs che contiene le informazioni per la registrazione del plug-in.</span><span class="sxs-lookup"><span data-stu-id="86fdc-112">The wizard generates a file with a .rgs file name extension that contains the information to register the plug-in with.</span></span> <span data-ttu-id="86fdc-113">Il valore "Capabilities" in questo file è l'equivalente decimale di un valore booleano o delle costanti del tipo di plug-in e dei flag di plug-in definiti in wmpplug. h.</span><span class="sxs-lookup"><span data-stu-id="86fdc-113">The "Capabilities" value in this file is the decimal equivalent of a Boolean OR of the plug-in type constants and plug-in flags defined in wmpplug.h.</span></span> <span data-ttu-id="86fdc-114">Sebbene questo valore sia determinato dalle opzioni selezionate nella procedura guidata, è necessario modificarlo se si desidera creare un plug-in con più set di impostazioni o uno a cui è possibile inviare elementi multimediali o playlist.</span><span class="sxs-lookup"><span data-stu-id="86fdc-114">Although this value is determined by the options you select in the wizard, you must modify it if you want to create a plug-in with multiple presets or one that media items or playlists can be sent to.</span></span>

<span data-ttu-id="86fdc-115">Quando si modifica ed estende il codice del plug-in, è possibile compilare e registrare la DLL in modo che sia possibile testare il plug-in in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="86fdc-115">As you modify and extend your plug-in code, you can build and register your DLL so that you can test your plug-in in Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86fdc-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86fdc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86fdc-117">**Creazione di un plug-in dell'interfaccia utente**</span><span class="sxs-lookup"><span data-stu-id="86fdc-117">**Building a UI Plug-in**</span></span>](building-a-ui-plug-in.md)
</dt> </dl>

 

 




