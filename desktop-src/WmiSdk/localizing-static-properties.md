---
description: È possibile localizzare le proprietà statiche usando le mappe di valori parziali.
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: Localizzazione di proprietà statiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecaba200b7880991d349c6e0c0196c88ffa54b11
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356164"
---
# <a name="localizing-static-properties"></a><span data-ttu-id="5df7f-103">Localizzazione di proprietà statiche</span><span class="sxs-lookup"><span data-stu-id="5df7f-103">Localizing Static Properties</span></span>

<span data-ttu-id="5df7f-104">È possibile localizzare le proprietà statiche usando le mappe di valori parziali.</span><span class="sxs-lookup"><span data-stu-id="5df7f-104">You can localize static properties by using partial value maps.</span></span>

<span data-ttu-id="5df7f-105">Nella procedura riportata di seguito viene descritto il modo in cui le proprietà statiche possono essere localizzate mediante mapping di valori parziali con espressioni regolari</span><span class="sxs-lookup"><span data-stu-id="5df7f-105">The following procedure describes how static properties can be localized using partial value maps with regular expressions.</span></span>

<span data-ttu-id="5df7f-106">**Per usare le mappe del valore per localizzare le proprietà statiche**</span><span class="sxs-lookup"><span data-stu-id="5df7f-106">**To use value maps to localize static properties**</span></span>

1.  <span data-ttu-id="5df7f-107">Creare un file MOF Master (Mastervm. MOF).</span><span class="sxs-lookup"><span data-stu-id="5df7f-107">Create a master MOF file (Mastervm.mof).</span></span>

    <span data-ttu-id="5df7f-108">L'esempio di codice seguente può essere utilizzato per creare un file MOF Master (Mastervm. MOF).</span><span class="sxs-lookup"><span data-stu-id="5df7f-108">The following code example can be used to create a master MOF file (Mastervm.mof).</span></span>

    ```syntax
    [Locale(0x409)]
    class Group1
    {
        [key] string ID;
        [DisplayName("Numbers"),
            ValueMap{0,1,2,3}:amended,
            Values{"Zero", "One", "Two", "Three"}:amended]
        Uint32 Numbers;
    };
    ```

2.  <span data-ttu-id="5df7f-109">Creare le versioni indipendente dalla lingua e dalla lingua del file MOF.</span><span class="sxs-lookup"><span data-stu-id="5df7f-109">Create the language-neutral and language-specific versions of the MOF file.</span></span>

    <span data-ttu-id="5df7f-110">Digitare il comando seguente al prompt dei comandi per creare le versioni del file MOF indipendenti dalla lingua e dal linguaggio.</span><span class="sxs-lookup"><span data-stu-id="5df7f-110">Type the following command at a command prompt to create the language-neutral and language-specific versions of the MOF file.</span></span>

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    <span data-ttu-id="5df7f-111">Il compilatore MOF genera i file MOF specifici del linguaggio e della lingua, LnVm. mof e LsVm. mfl.</span><span class="sxs-lookup"><span data-stu-id="5df7f-111">The MOF compiler generates the language-specific and language-neutral MOF files, LnVm.mof and LsVm.mfl.</span></span> <span data-ttu-id="5df7f-112">I valori della lingua inglese (Stati Uniti) per la proprietà [numbers](numbers.md) vengono inseriti nel file con estensione MFL per lo spazio dei nomi American English.</span><span class="sxs-lookup"><span data-stu-id="5df7f-112">The American English values for the [Numbers](numbers.md) property is placed in the .mfl file for the American English namespace.</span></span>

    <span data-ttu-id="5df7f-113">Nell'esempio di codice seguente viene illustrato il contenuto del file LsVm. mfl.</span><span class="sxs-lookup"><span data-stu-id="5df7f-113">The following code example shows the contents of the LsVm.mfl file.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_409";};
    #pragma namespace("\\\\.\\root\\default\\ms_409")

    [AMENDMENT, LOCALE(0x409)] 
    class Group1
    {
      [ValueMap{0, 1, 2, 3} : Amended,
          Values{"Zero", "One", "Two", "Three"} : Amended] 
      Uint32 Numbers;
    };
    ```

3.  <span data-ttu-id="5df7f-114">Compilare i due file MOF e archiviare le informazioni sulla classe nel repository CIM.</span><span class="sxs-lookup"><span data-stu-id="5df7f-114">Compile the two MOF files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="5df7f-115">Digitare il comando seguente al prompt dei comandi per compilare i due file MOF.</span><span class="sxs-lookup"><span data-stu-id="5df7f-115">Type the following command at a command prompt to compile the two MOF files.</span></span>

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  <span data-ttu-id="5df7f-116">Localizzare il file MFL per altre impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="5df7f-116">Localize the MFL file for other locales.</span></span>

    <span data-ttu-id="5df7f-117">Nell'esempio di codice seguente viene illustrato il contenuto di un file MFL per lo spazio dei nomi francese.</span><span class="sxs-lookup"><span data-stu-id="5df7f-117">The following code example shows the contents of an MFL file for the French namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_40C";};
    #pragma namespace("\\\\.\\root\\default\\ms_40C")

    [AMENDMENT, LOCALE(0x40C)] 
    class Group1
    {
        [key] string ID;
        [ValueMap{0, 1, 2, 3} : Amended,
            Values{"Zero", "Un", "Deux", "Trois"} : Amended]
        Uint32 Numbers;
    };
    ```

<span data-ttu-id="5df7f-118">Il risultato finale è che il nome visualizzato e il valore della proprietà [numbers](numbers.md) dipendono dalle impostazioni locali dell'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="5df7f-118">The net result is that both the display name and the value of the [Numbers](numbers.md) property depend on the locale of the logged-on user.</span></span> <span data-ttu-id="5df7f-119">Se l'utente specifica le impostazioni locali che non sono state specificate, i dati di qualificatore predefiniti provengono dallo \_ spazio dei nomi inglese (ms 409).</span><span class="sxs-lookup"><span data-stu-id="5df7f-119">If the user specifies a locale that has not been provided, the default qualifier data comes from the English (ms\_409) namespace.</span></span>

<span data-ttu-id="5df7f-120">L'implicazione di questa progettazione è che ogni valore di stringa viene utilizzato come identificatore di ricerca, che non può essere localizzato.</span><span class="sxs-lookup"><span data-stu-id="5df7f-120">The implication of this design is that each string value is used as a lookup identifier, which cannot be localized.</span></span> <span data-ttu-id="5df7f-121">Quando si definisce questo schema, è necessario assicurarsi che il valore inserito dal provider sia indipendente dalle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="5df7f-121">When defining this scheme, you must ensure that the value the provider puts in is locale-independent.</span></span>

> [!Note]  
> <span data-ttu-id="5df7f-122">In WMI non è attualmente disponibile il supporto in fase di esecuzione per il mapping di valori a stringhe definite da qualificatori.</span><span class="sxs-lookup"><span data-stu-id="5df7f-122">WMI does not currently provide run-time support for mapping values to strings defined by qualifiers.</span></span> <span data-ttu-id="5df7f-123">L'interpretazione della sintassi suggerita è responsabilità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5df7f-123">Interpretation of the suggested syntax is the application's responsibility.</span></span>

 

 

 



