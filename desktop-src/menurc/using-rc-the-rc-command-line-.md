---
title: Using RC (The RC Command Line) (Uso di RC - Riga di comando RC)
description: Per avviare RC, utilizzare il comando seguente.
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34e24fdf7b9b648a9baf9c6db8981f05d5434ef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963010"
---
# <a name="using-rc-the-rc-command-line"></a><span data-ttu-id="930e7-103">Using RC (The RC Command Line) (Uso di RC - Riga di comando RC)</span><span class="sxs-lookup"><span data-stu-id="930e7-103">Using RC (The RC Command Line)</span></span>

<span data-ttu-id="930e7-104">Per avviare RC, utilizzare il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="930e7-104">To start RC, use the following command.</span></span>

<span data-ttu-id="930e7-105">**RC** \[ *Opzioni* \] di *script-file*</span><span class="sxs-lookup"><span data-stu-id="930e7-105">**RC** \[*options*\] *script-file*</span></span>

<span data-ttu-id="930e7-106">Il parametro *script-file* specifica il nome del file di definizione delle risorse che contiene i nomi, i tipi, i nomi di file e le descrizioni delle risorse da compilare.</span><span class="sxs-lookup"><span data-stu-id="930e7-106">The *script-file* parameter specifies the name of the resource-definition file that contains the names, types, filenames, and descriptions of the resources to be compiled.</span></span>

<span data-ttu-id="930e7-107">RC può generare file di risorse separati per le applicazioni che dispongono di risorse sia indipendenti dalla lingua che specifiche della lingua.</span><span class="sxs-lookup"><span data-stu-id="930e7-107">RC can generate separate resource files for applications that have both language-neutral and language-specific resources.</span></span> <span data-ttu-id="930e7-108">Gli sviluppatori possono usare un [file di configurazione delle risorse](/windows/desktop/Intl/preparing-resources) o impostare le opzioni della riga di comando per selezionare i tipi di risorse e gli elementi che sono risorse non localizzabili del [file indipendente dalla lingua](/windows/desktop/Intl/mui-resource-management) e che sono risorse localizzabili dei file MUI specifici della lingua.</span><span class="sxs-lookup"><span data-stu-id="930e7-108">Developers can use a [resource configuration file](/windows/desktop/Intl/preparing-resources) or set command-line options to select which resource types and items are non-localizable resources of the [language-neutral (LN) file](/windows/desktop/Intl/mui-resource-management) and which are localizable resources of language-specific MUI files.</span></span> <span data-ttu-id="930e7-109">Per ulteriori informazioni, vedere l' [interfaccia utente multilingue](/windows/desktop/Intl/multilingual-user-interface).</span><span class="sxs-lookup"><span data-stu-id="930e7-109">For more information, see the [Multilingual User Interface](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="930e7-110">Il parametro *options* può essere costituito da una o più delle seguenti opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="930e7-110">The *options* parameter can be one or more of the following command-line options.</span></span>

## <a name="options"></a><span data-ttu-id="930e7-111">Opzioni</span><span class="sxs-lookup"><span data-stu-id="930e7-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="930e7-112"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="930e7-112"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="930e7-113">Visualizza un elenco di opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="930e7-113">Displays a list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-114"><span id="_c"></span><span id="_C"></span>**/c**</span><span class="sxs-lookup"><span data-stu-id="930e7-114"><span id="_c"></span><span id="_C"></span>**/c**</span></span>
</dt> <dd>

<span data-ttu-id="930e7-115">Definisce una tabella codici utilizzata dalla conversione NLS.</span><span class="sxs-lookup"><span data-stu-id="930e7-115">Defines a code page used by NLS conversion.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-116"><span id="_d"></span><span id="_D"></span>**/d**</span><span class="sxs-lookup"><span data-stu-id="930e7-116"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="930e7-117">Definisce un simbolo per il preprocessore che è possibile testare con la direttiva [**\# ifdef**](-ifdef.md) .</span><span class="sxs-lookup"><span data-stu-id="930e7-117">Defines a symbol for the preprocessor that you can test with the [**\#ifdef**](-ifdef.md) directive.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span> *mresname* /FM</span><span class="sxs-lookup"><span data-stu-id="930e7-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/fm** *mresname*</span></span>
</dt> <dd>

<span data-ttu-id="930e7-119">RC crea una lingua indipendente dalla lingua. File RES e uno dipendente dalla lingua (MUI). File RES tramite *script-file*.</span><span class="sxs-lookup"><span data-stu-id="930e7-119">RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file using *script-file*.</span></span> <span data-ttu-id="930e7-120">Questa opzione deve essere usata insieme all'opzione **/fo** *resName*</span><span class="sxs-lookup"><span data-stu-id="930e7-120">This option must be used together with the **/fo** *resname* option.</span></span> <span data-ttu-id="930e7-121">RC assegna un nome indipendente dalla lingua. RES file *resName. res* e assegna un nome al linguaggio MUI. File RES *mresname. res*.</span><span class="sxs-lookup"><span data-stu-id="930e7-121">RC names the language-neutral .RES file *resname.res* and names the language-dependent (MUI) .RES file *mresname.res*.</span></span>

<span data-ttu-id="930e7-122">**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le funzioni [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.</span><span class="sxs-lookup"><span data-stu-id="930e7-122">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span> *resName* /fo</span><span class="sxs-lookup"><span data-stu-id="930e7-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*</span></span>
</dt> <dd>

<span data-ttu-id="930e7-124">RC crea un oggetto. File RES denominato *resName* con *script-file*.</span><span class="sxs-lookup"><span data-stu-id="930e7-124">RC creates a .RES file named *resname* using *script-file*.</span></span>

<span data-ttu-id="930e7-125">Se viene impostata anche l'opzione **/FM** *mresname* , RC crea una lingua indipendente dalla lingua. File RES e uno dipendente dalla lingua (MUI). File RES.</span><span class="sxs-lookup"><span data-stu-id="930e7-125">If the **/fm** *mresname* option is also set, RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file.</span></span>

<span data-ttu-id="930e7-126">**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le funzioni [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.</span><span class="sxs-lookup"><span data-stu-id="930e7-126">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-127"><span id="_g1"></span><span id="_G1"></span>**/G1**</span><span class="sxs-lookup"><span data-stu-id="930e7-127"><span id="_g1"></span><span id="_G1"></span>**/g1**</span></span>
</dt> <dd>

<span data-ttu-id="930e7-128">Se/G1 è impostato, RC genera un file MUI se l'unica risorsa localizzabile che viene inclusa nel file MUI è una risorsa della versione.</span><span class="sxs-lookup"><span data-stu-id="930e7-128">If /g1, is set, RC generates a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span> <span data-ttu-id="930e7-129">Se/G1 non è impostato, RC non genererà un file MUI se l'unica risorsa localizzabile inclusa nel file MUI è una risorsa della versione.</span><span class="sxs-lookup"><span data-stu-id="930e7-129">If /g1 is not set, RC will not generate a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-130"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="930e7-130"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="930e7-131">Visualizza l'elenco delle opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="930e7-131">Displays the list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-132"><span id="_I"></span><span id="_i"></span>**/I**</span><span class="sxs-lookup"><span data-stu-id="930e7-132"><span id="_I"></span><span id="_i"></span>**/I**</span></span>
</dt> <dd>

<span data-ttu-id="930e7-133">Cerca nella directory specificata prima di cercare le directory specificate dalla variabile di ambiente INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="930e7-133">Searches the specified directory before searching the directories specified by the INCLUDE environment variable.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span> *loctype* /j</span><span class="sxs-lookup"><span data-stu-id="930e7-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*</span></span>
</dt> <dd>

<span data-ttu-id="930e7-135">I tipi di risorsa localizzabili RC vengono posizionati nel linguaggio MUI (Language-dipendente). File RES.</span><span class="sxs-lookup"><span data-stu-id="930e7-135">Localizable resource types RC places into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="930e7-136">Se si imposta anche l'opzione **/q** , questa opzione viene ignorata e le informazioni nel file di configurazione RC hanno la precedenza.</span><span class="sxs-lookup"><span data-stu-id="930e7-136">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="930e7-137">**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le funzioni [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.</span><span class="sxs-lookup"><span data-stu-id="930e7-137">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>sovratipo **/k** </span><span class="sxs-lookup"><span data-stu-id="930e7-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *overtype*</span></span>
</dt> <dd>

<span data-ttu-id="930e7-139">Tipi di risorse sovrapposti che RC inserisce in entrambi i tipi di risorse indipendenti dalla lingua. RES e la lingua dipendente (MUI). File RES.</span><span class="sxs-lookup"><span data-stu-id="930e7-139">Overlapping resource types that RC places into both the language-neutral .RES and the language-dependent (MUI).RES files.</span></span> <span data-ttu-id="930e7-140">I tipi di risorsa specificati dall'opzione **/k** devono essere un subset di quelli specificati dall'opzione **/j** .</span><span class="sxs-lookup"><span data-stu-id="930e7-140">The resource types that are specified by the **/k** option must be a subset of those that are specified by the **/j** option.</span></span> <span data-ttu-id="930e7-141">Per esempio? J2? J3? K3 specifica che RC inserisce il tipo di risorsa 3 in entrambi i file indipendenti dalla lingua e dalla lingua (MUI).</span><span class="sxs-lookup"><span data-stu-id="930e7-141">For example, ?J2 ?J3 ?K3 specifies that RC places resource type 3 in both the language-neutral and language-dependent (MUI) files.</span></span> <span data-ttu-id="930e7-142">Se si imposta anche l'opzione **/q** , questa opzione viene ignorata e le informazioni nel file di configurazione RC hanno la precedenza.</span><span class="sxs-lookup"><span data-stu-id="930e7-142">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="930e7-143">**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le funzioni [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.</span><span class="sxs-lookup"><span data-stu-id="930e7-143">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *LangID*</span><span class="sxs-lookup"><span data-stu-id="930e7-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*</span></span>
</dt> <dd>

<span data-ttu-id="930e7-145">Specifica la lingua predefinita per la compilazione.</span><span class="sxs-lookup"><span data-stu-id="930e7-145">Specifies the default language for compilation.</span></span> <span data-ttu-id="930e7-146">Ad esempio,-L409 equivale a includere l'istruzione seguente all'inizio del file di script di risorsa: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span><span class="sxs-lookup"><span data-stu-id="930e7-146">For example, -l409 is equivalent to including the following statement at the top of the resource script file: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span></span>

<span data-ttu-id="930e7-147">Per ulteriori informazioni, vedere [identificatori di lingua](/windows/desktop/Intl/language-identifiers).</span><span class="sxs-lookup"><span data-stu-id="930e7-147">For more information, see [Language Identifiers](/windows/desktop/Intl/language-identifiers).</span></span>

</dd> <dt>

<span data-ttu-id="930e7-148"><span id="_n"></span><span id="_N"></span>**/n**</span><span class="sxs-lookup"><span data-stu-id="930e7-148"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="930e7-149">Null termina tutte le stringhe nella tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="930e7-149">Null terminates all strings in the string table.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/Q** *MUI. rcconfig*</span><span class="sxs-lookup"><span data-stu-id="930e7-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/q** *Mui.RCConfig*</span></span>
</dt> <dd>

<span data-ttu-id="930e7-151">Un file di configurazione RC che segue il formato del file di configurazione RC.</span><span class="sxs-lookup"><span data-stu-id="930e7-151">An RC configuration file that follows the RC Configuration File format.</span></span> <span data-ttu-id="930e7-152">Il formato del file di configurazione RC consente ai componenti di descrivere autonomamente le informazioni sulle risorse, ad esempio il controllo delle versioni delle risorse, il percorso file MUI, i tipi di risorse e gli elementi</span><span class="sxs-lookup"><span data-stu-id="930e7-152">The RC Configuration File format enables components to self-describe resource information such as resource versioning, MUI file path, resource types and items.</span></span> <span data-ttu-id="930e7-153">Questo file specifica quali risorse vengono inserite nella lingua indipendente dalla lingua. File RES e quali risorse vengono inserite nel linguaggio MUI (dipendente dalla lingua). File RES.</span><span class="sxs-lookup"><span data-stu-id="930e7-153">This file specifies which resources go into the language-neutral .RES file and which resources go into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="930e7-154">Questa opzione e le informazioni fornite nel file di configurazione RC eseguono l'override delle opzioni della riga di comando **/j** e **/k**.</span><span class="sxs-lookup"><span data-stu-id="930e7-154">This option, and the information provided in the RC Configuration file, override the command line options **/j** and **/k**.</span></span>

<span data-ttu-id="930e7-155">**Windows Server 2003 e Windows XP/2000:** Questa opzione non è disponibile senza usare anche le funzioni [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) e [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) in un sistema aggiornato.</span><span class="sxs-lookup"><span data-stu-id="930e7-155">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-156"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="930e7-156"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="930e7-157">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="930e7-157">Ignored.</span></span> <span data-ttu-id="930e7-158">Fornito per la compatibilità con i makefile esistenti.</span><span class="sxs-lookup"><span data-stu-id="930e7-158">Provided for compatibility with existing makefiles.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-159"><span id="_u"></span><span id="_U"></span>**/u**</span><span class="sxs-lookup"><span data-stu-id="930e7-159"><span id="_u"></span><span id="_U"></span>**/u**</span></span>
</dt> <dd>

<span data-ttu-id="930e7-160">Definisce un simbolo per il preprocessore.</span><span class="sxs-lookup"><span data-stu-id="930e7-160">Undefines a symbol for the preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-161"><span id="_v"></span><span id="_V"></span>**/v**</span><span class="sxs-lookup"><span data-stu-id="930e7-161"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="930e7-162">Visualizza i messaggi che segnalano lo stato di avanzamento del compilatore.</span><span class="sxs-lookup"><span data-stu-id="930e7-162">Displays messages that report on the progress of the compiler.</span></span>

</dd> <dt>

<span data-ttu-id="930e7-163"><span id="_x"></span><span id="_X"></span>**/x**</span><span class="sxs-lookup"><span data-stu-id="930e7-163"><span id="_x"></span><span id="_X"></span>**/x**</span></span>
</dt> <dd>

<span data-ttu-id="930e7-164">Impedisce a RC di controllare la variabile di ambiente INCLUDE durante la ricerca di file di intestazione o di risorse.</span><span class="sxs-lookup"><span data-stu-id="930e7-164">Prevents RC from checking the INCLUDE environment variable when searching for header files or resource files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="930e7-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="930e7-165">Remarks</span></span>

<span data-ttu-id="930e7-166">Le opzioni non distinguono tra maiuscole e minuscole e il segno meno (-) può essere utilizzato al posto di una barra (/).</span><span class="sxs-lookup"><span data-stu-id="930e7-166">Options are not case sensitive, and a hyphen (-) can be used in place of a slash mark (/).</span></span> <span data-ttu-id="930e7-167">È possibile combinare le opzioni di una singola lettera se non richiedono parametri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="930e7-167">You can combine single-letter options if they do not require any additional parameters.</span></span>

<span data-ttu-id="930e7-168">RC non genererà un file MUI nei casi seguenti.</span><span class="sxs-lookup"><span data-stu-id="930e7-168">RC will not generate a MUI file in the following cases.</span></span>

-   <span data-ttu-id="930e7-169">Nel file RC non esistono risorse localizzabili.</span><span class="sxs-lookup"><span data-stu-id="930e7-169">No localizable resources exist in the .rc file.</span></span>
-   <span data-ttu-id="930e7-170">L'unico ID lingua della risorsa specificato nel file RC è neutro (0x0).</span><span class="sxs-lookup"><span data-stu-id="930e7-170">The only resource language id specified in the .rc file is neutral (0x0).</span></span>
-   <span data-ttu-id="930e7-171">Il file RC contiene risorse specificate in più di una lingua.</span><span class="sxs-lookup"><span data-stu-id="930e7-171">The .rc file has resources that are specified in more than one language.</span></span> <span data-ttu-id="930e7-172">L'eccezione è rappresentata dal caso in cui il file RC contenga due lingue e una lingua è neutra (0x0), RC genera un file MUI.</span><span class="sxs-lookup"><span data-stu-id="930e7-172">The exception is if the .rc file contains two languages, and one language is neutral (0x0), RC generates a MUI file.</span></span>

<span data-ttu-id="930e7-173">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="930e7-173">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="930e7-174">Definizione dei nomi per il preprocessore</span><span class="sxs-lookup"><span data-stu-id="930e7-174">Defining Names for the Preprocessor</span></span>](defining-names-for-the-preprocessor.md)
-   [<span data-ttu-id="930e7-175">Ridenominazione del file di risorse compilato</span><span class="sxs-lookup"><span data-stu-id="930e7-175">Renaming the Compiled Resource File</span></span>](renaming-the-compiled-resource-file.md)
-   [<span data-ttu-id="930e7-176">Ricerca di file</span><span class="sxs-lookup"><span data-stu-id="930e7-176">Searching for Files</span></span>](searching-for-files.md)
-   [<span data-ttu-id="930e7-177">Visualizzazione dei messaggi di stato</span><span class="sxs-lookup"><span data-stu-id="930e7-177">Displaying Progress Messages</span></span>](displaying-progress-messages.md)
-   [<span data-ttu-id="930e7-178">Messaggi di diagnostica RC</span><span class="sxs-lookup"><span data-stu-id="930e7-178">RC Diagnostic Messages</span></span>](rc-diagnostic-messages.md)

## <a name="related-topics"></a><span data-ttu-id="930e7-179">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="930e7-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="930e7-180">Interfaccia utente multilingue</span><span class="sxs-lookup"><span data-stu-id="930e7-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 