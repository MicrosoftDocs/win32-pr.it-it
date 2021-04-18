---
description: Il controllo WMI è uno snap-in di MMC disponibile nel pannello di controllo e viene utilizzato per impostare manualmente la sicurezza dello spazio dei nomi WMI in un computer locale. È inoltre possibile impostare lo spazio dei nomi predefinito per lo scripting.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Impostazione della sicurezza dello spazio dei nomi con il controllo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e8b6ed7c45b6b0d107f7f4e4b92f31f504900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318526"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a><span data-ttu-id="dec1b-104">Impostazione della sicurezza dello spazio dei nomi con il controllo WMI</span><span class="sxs-lookup"><span data-stu-id="dec1b-104">Setting Namespace Security with the WMI Control</span></span>

<span data-ttu-id="dec1b-105">Il controllo WMI è uno snap-in di MMC disponibile nel **Pannello di controllo** e viene utilizzato per impostare manualmente la sicurezza dello spazio dei nomi WMI in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="dec1b-105">The WMI Control is an MMC snap-in located in the **Control Panel** and is used to set WMI namespace security manually on a local computer.</span></span> <span data-ttu-id="dec1b-106">È inoltre possibile impostare lo spazio dei nomi predefinito per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="dec1b-106">You can also set the default namespace for scripting.</span></span>


<span data-ttu-id="dec1b-107">Nella procedura riportata di seguito viene descritto come individuare il controllo WMI.</span><span class="sxs-lookup"><span data-stu-id="dec1b-107">The following procedure describes how to locate the WMI Control.</span></span>

<span data-ttu-id="dec1b-108">**Per individuare il controllo WMI**</span><span class="sxs-lookup"><span data-stu-id="dec1b-108">**To locate the WMI control**</span></span>

1.  <span data-ttu-id="dec1b-109">Nel **Pannello di controllo** fare doppio clic su **strumenti di amministrazione**.</span><span class="sxs-lookup"><span data-stu-id="dec1b-109">In the **Control Panel**, double-click **Administrative Tools**.</span></span>
2.  <span data-ttu-id="dec1b-110">Nella finestra **Strumenti di amministrazione** fare doppio clic su **Gestione computer**.</span><span class="sxs-lookup"><span data-stu-id="dec1b-110">In the **Administrative Tools** window, double-click **Computer Management**.</span></span>
3.  <span data-ttu-id="dec1b-111">Nella finestra **Gestione computer** espandere l'albero **Servizi e applicazioni** , quindi fare doppio clic sul **controllo WMI**.</span><span class="sxs-lookup"><span data-stu-id="dec1b-111">In the **Computer Management** window, expand the **Services and Applications** tree and double-click the **WMI Control**.</span></span>
4.  <span data-ttu-id="dec1b-112">Fare clic con il pulsante destro del mouse sull'icona del **controllo WMI** e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="dec1b-112">Right-click the **WMI Control** icon and select **Properties**.</span></span>

<span data-ttu-id="dec1b-113">Nella procedura seguente viene descritto come utilizzare il controllo WMI per configurare la sicurezza per uno spazio dei nomi come modello, quindi ottenere a livello di codice le impostazioni di sicurezza per impostare la sicurezza per altri spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="dec1b-113">The following procedure describes how to use the WMI control to set up the security for a namespace as a template, then programmatically obtain the security settings to set security for other namespaces.</span></span>

<span data-ttu-id="dec1b-114">**Per impostare la sicurezza dello spazio dei nomi con il controllo WMI**</span><span class="sxs-lookup"><span data-stu-id="dec1b-114">**To set namespace security with the WMI control**</span></span>

1.  <span data-ttu-id="dec1b-115">Creare un nuovo spazio dei nomi utilizzando il codice Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="dec1b-115">Create a new namespace by using Managed Object Format (MOF) code.</span></span>
2.  <span data-ttu-id="dec1b-116">Eseguire il controllo WMI per impostare la sicurezza del nuovo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="dec1b-116">Run the WMI Control to set the security on the new namespace.</span></span> <span data-ttu-id="dec1b-117">Dal menu **Start** fare clic su **Esegui** e digitare **wmimgmt. msc** o vedere [individuazione del controllo WMI](#).</span><span class="sxs-lookup"><span data-stu-id="dec1b-117">On the **Start** menu, click **Run** and type **wmimgmt.msc** or see [Locating the WMI Control](#).</span></span>
3.  <span data-ttu-id="dec1b-118">Nel riquadro di **controllo WMI** fare clic con il pulsante destro del mouse su **controllo WMI**, scegliere **Proprietà**, quindi selezionare la scheda **sicurezza** .</span><span class="sxs-lookup"><span data-stu-id="dec1b-118">In the **WMI Control** pane, right-click **WMI Control**, choose **Properties**, and then select the **Security** tab.</span></span>
4.  <span data-ttu-id="dec1b-119">Passare al nuovo spazio dei nomi, fare clic su **sicurezza** e quindi configurare gruppi e autorizzazioni per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="dec1b-119">Navigate to the new namespace, click **Security**, and then configure groups and permissions for the namespace.</span></span>

<span data-ttu-id="dec1b-120">È inoltre possibile utilizzare Strumentazione gestione Windows Command-Line ([wmic](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) per impostare la sicurezza dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="dec1b-120">You can also use Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) to set namespace security.</span></span> <span data-ttu-id="dec1b-121">Per ulteriori informazioni, vedere [**wmic**](wmic.md).</span><span class="sxs-lookup"><span data-stu-id="dec1b-121">For more information, see [**wmic**](wmic.md).</span></span>

## <a name="setting-the-default-namespace-for-scripts"></a><span data-ttu-id="dec1b-122">Impostazione dello spazio dei nomi predefinito per gli script</span><span class="sxs-lookup"><span data-stu-id="dec1b-122">Setting the Default Namespace for Scripts</span></span>

<span data-ttu-id="dec1b-123">Se uno script non si connette in modo esplicito a uno spazio dei nomi durante la connessione a WMI, WMI utilizza lo spazio dei nomi predefinito specificato in questo controllo.</span><span class="sxs-lookup"><span data-stu-id="dec1b-123">If a script does not connect explicitly to a namespace when connecting to WMI, then WMI uses the default namespace specified in this control.</span></span> <span data-ttu-id="dec1b-124">Il valore predefinito è disponibile anche nella voce del registro di sistema, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="dec1b-124">The default is also found in the registry entry as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

<span data-ttu-id="dec1b-125">Poiché lo spazio dei nomi predefinito è facile da modificare, con questo controllo o a livello di codice chiamando i metodi di [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), specificare lo spazio dei nomi durante la connessione a WMI tramite il [moniker](constructing-a-moniker-string.md) o le chiamate a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="dec1b-125">Because the default namespace is easy to change, either with this control or programmatically by calling methods of [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), specify the namespace when connecting to WMI either through the [moniker](constructing-a-moniker-string.md) or calls to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="dec1b-126">Per ulteriori informazioni, vedere [creazione di uno script WMI](creating-a-wmi-script.md)</span><span class="sxs-lookup"><span data-stu-id="dec1b-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md)</span></span>

<span data-ttu-id="dec1b-127">**Per impostare lo spazio dei nomi predefinito per gli script**</span><span class="sxs-lookup"><span data-stu-id="dec1b-127">**To set the default namespace for scripts**</span></span>

1.  <span data-ttu-id="dec1b-128">Nella finestra **proprietà del controllo WMI** scegliere la scheda **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="dec1b-128">In the **WMI Control Properties** window, choose the **Advanced** tab.</span></span>
2.  <span data-ttu-id="dec1b-129">Fare clic sul pulsante **Cambia** e selezionare lo spazio dei nomi da impostare come predefinito.</span><span class="sxs-lookup"><span data-stu-id="dec1b-129">Click the **Change** button and select the namespace to make the default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dec1b-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dec1b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dec1b-131">Impostazione di descrittori di sicurezza dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dec1b-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
