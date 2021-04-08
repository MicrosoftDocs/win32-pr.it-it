---
description: I modelli definiscono il modo in cui il flusso di dati viene interpretato. i dati vengono modulati dalla definizione del modello. In questa sezione vengono illustrati i seguenti aspetti di un modello e viene fornito un modello di esempio.
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Modelli (formato di file X, codifica del testo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fccec46e72a73bb5ed4434fd252595e1b072ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745391"
---
# <a name="templates-x-file-format-text-encoding"></a><span data-ttu-id="04499-104">Modelli (formato di file X, codifica del testo)</span><span class="sxs-lookup"><span data-stu-id="04499-104">Templates (X file format, text encoding)</span></span>

<span data-ttu-id="04499-105">I modelli definiscono il modo in cui il flusso di dati viene interpretato. i dati vengono modulati dalla definizione del modello.</span><span class="sxs-lookup"><span data-stu-id="04499-105">Templates define how the data stream is interpreted - the data is modulated by the template definition.</span></span> <span data-ttu-id="04499-106">In questa sezione vengono illustrati i seguenti aspetti di un modello e viene fornito un modello di esempio.</span><span class="sxs-lookup"><span data-stu-id="04499-106">This section discusses the following aspects of a template and provides an example template.</span></span>

<span data-ttu-id="04499-107">È disponibile un modello speciale, ovvero il modello di intestazione.</span><span class="sxs-lookup"><span data-stu-id="04499-107">There is one special template - the header template.</span></span> <span data-ttu-id="04499-108">È consigliabile che ogni applicazione definisca un modello di intestazione e lo usi per definire informazioni specifiche dell'applicazione, ad esempio le informazioni sulla versione.</span><span class="sxs-lookup"><span data-stu-id="04499-108">It is recommended that each application define a header template and use it to define application-specific information, such as version information.</span></span> <span data-ttu-id="04499-109">Se presente, questa intestazione viene letta dall'API del formato di file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="04499-109">If present, this header is read by the .x file format API.</span></span> <span data-ttu-id="04499-110">Se è disponibile un membro dei flag, viene usato per determinare come vengono interpretati i dati seguenti.</span><span class="sxs-lookup"><span data-stu-id="04499-110">If a flags member is available, it is used to determine how the following data is interpreted.</span></span> <span data-ttu-id="04499-111">Il membro dei flag, se definito, deve essere un valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="04499-111">The flags member, if defined, should be a DWORD.</span></span> <span data-ttu-id="04499-112">Un bit è attualmente definito a bit 0.</span><span class="sxs-lookup"><span data-stu-id="04499-112">One bit is currently defined - bit 0.</span></span> <span data-ttu-id="04499-113">Se questo bit è chiaro, i dati seguenti nel file sono binari.</span><span class="sxs-lookup"><span data-stu-id="04499-113">If this bit is clear, the following data in the file is binary.</span></span> <span data-ttu-id="04499-114">Se impostata, i dati seguenti sono di testo.</span><span class="sxs-lookup"><span data-stu-id="04499-114">If set, the following data is text.</span></span> <span data-ttu-id="04499-115">È possibile utilizzare più oggetti dati di intestazione per passare da un file binario a un testo all'interno del file.</span><span class="sxs-lookup"><span data-stu-id="04499-115">You can use multiple header data objects to switch between binary and text within the file.</span></span>

## <a name="template-form-name-and-uuid"></a><span data-ttu-id="04499-116">Form modello, nome e UUID</span><span class="sxs-lookup"><span data-stu-id="04499-116">Template Form, Name, and UUID</span></span>

<span data-ttu-id="04499-117">Un modello ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="04499-117">A template has the following form.</span></span>


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



<span data-ttu-id="04499-118">Il nome del modello è un nome alfanumerico che può includere il carattere di sottolineatura ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="04499-118">The template name is an alphanumeric name that can include the underscore character (\_).</span></span> <span data-ttu-id="04499-119">Non deve iniziare con una cifra.</span><span class="sxs-lookup"><span data-stu-id="04499-119">It must not begin with a digit.</span></span> <span data-ttu-id="04499-120">UUID è un identificatore univoco universale formattato per l'ambiente di elaborazione distribuita Open Software Foundation standard e racchiuso tra parentesi acute (< >).</span><span class="sxs-lookup"><span data-stu-id="04499-120">The UUID is a universally unique identifier formatted to the Open Software Foundation's Distributed Computing Environment standard and enclosed by angle brackets (< >).</span></span> <span data-ttu-id="04499-121">Ad esempio: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.</span><span class="sxs-lookup"><span data-stu-id="04499-121">For example: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.</span></span>

## <a name="template-members"></a><span data-ttu-id="04499-122">Membri del modello</span><span class="sxs-lookup"><span data-stu-id="04499-122">Template Members</span></span>

<span data-ttu-id="04499-123">I membri del modello sono costituiti da un tipo di dati denominato seguito da un nome facoltativo o da una matrice di un tipo di dati denominato.</span><span class="sxs-lookup"><span data-stu-id="04499-123">Template members consist of a named data type followed by an optional name or an array of a named data type.</span></span> <span data-ttu-id="04499-124">I tipi di dati primitivi validi sono definiti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="04499-124">Valid primitive data types are defined in the following table.</span></span>



| <span data-ttu-id="04499-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="04499-125">Type</span></span>    | <span data-ttu-id="04499-126">Dimensione</span><span class="sxs-lookup"><span data-stu-id="04499-126">Size</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="04499-127">WORD</span><span class="sxs-lookup"><span data-stu-id="04499-127">WORD</span></span>    | <span data-ttu-id="04499-128">16 bit</span><span class="sxs-lookup"><span data-stu-id="04499-128">16 bits</span></span>                            |
| <span data-ttu-id="04499-129">DWORD</span><span class="sxs-lookup"><span data-stu-id="04499-129">DWORD</span></span>   | <span data-ttu-id="04499-130">32 bit</span><span class="sxs-lookup"><span data-stu-id="04499-130">32 bits</span></span>                            |
| <span data-ttu-id="04499-131">FLOAT</span><span class="sxs-lookup"><span data-stu-id="04499-131">FLOAT</span></span>   | <span data-ttu-id="04499-132">IEEE float</span><span class="sxs-lookup"><span data-stu-id="04499-132">IEEE float</span></span>                         |
| <span data-ttu-id="04499-133">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="04499-133">DOUBLE</span></span>  | <span data-ttu-id="04499-134">64 bit</span><span class="sxs-lookup"><span data-stu-id="04499-134">64 bits</span></span>                            |
| <span data-ttu-id="04499-135">CHAR</span><span class="sxs-lookup"><span data-stu-id="04499-135">CHAR</span></span>    | <span data-ttu-id="04499-136">8 bit</span><span class="sxs-lookup"><span data-stu-id="04499-136">8 bits</span></span>                             |
| <span data-ttu-id="04499-137">UCHAR</span><span class="sxs-lookup"><span data-stu-id="04499-137">UCHAR</span></span>   | <span data-ttu-id="04499-138">8 bit</span><span class="sxs-lookup"><span data-stu-id="04499-138">8 bits</span></span>                             |
| <span data-ttu-id="04499-139">BYTE</span><span class="sxs-lookup"><span data-stu-id="04499-139">BYTE</span></span>    | <span data-ttu-id="04499-140">8 bit</span><span class="sxs-lookup"><span data-stu-id="04499-140">8 bits</span></span>                             |
| <span data-ttu-id="04499-141">STRING</span><span class="sxs-lookup"><span data-stu-id="04499-141">STRING</span></span>  | <span data-ttu-id="04499-142">Stringa con terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="04499-142">NULL terminated string</span></span>             |
| <span data-ttu-id="04499-143">CSTRING</span><span class="sxs-lookup"><span data-stu-id="04499-143">CSTRING</span></span> | <span data-ttu-id="04499-144">Stringa C formattata (non supportata)</span><span class="sxs-lookup"><span data-stu-id="04499-144">Formatted C string (not supported)</span></span> |
| <span data-ttu-id="04499-145">UNICODE</span><span class="sxs-lookup"><span data-stu-id="04499-145">UNICODE</span></span> | <span data-ttu-id="04499-146">Stringa Unicode (non supportata)</span><span class="sxs-lookup"><span data-stu-id="04499-146">Unicode string (not supported)</span></span>     |



 

<span data-ttu-id="04499-147">È anche possibile fare riferimento ai tipi di dati aggiuntivi definiti dai modelli rilevati in precedenza nel flusso di dati all'interno di una definizione di modello.</span><span class="sxs-lookup"><span data-stu-id="04499-147">Additional data types defined by templates encountered earlier in the data stream can also be referenced within a template definition.</span></span> <span data-ttu-id="04499-148">Non sono consentiti riferimenti in futuro.</span><span class="sxs-lookup"><span data-stu-id="04499-148">No forward references are allowed.</span></span>

<span data-ttu-id="04499-149">Qualsiasi tipo di dati valido può essere espresso come matrice nella definizione del modello.</span><span class="sxs-lookup"><span data-stu-id="04499-149">Any valid data type can be expressed as an array in the template definition.</span></span> <span data-ttu-id="04499-150">Nell'esempio seguente viene illustrata la sintassi di base.</span><span class="sxs-lookup"><span data-stu-id="04499-150">The basic syntax is shown in the following example.</span></span>


```
array <data-type> <name>[<dimension-size>];
```



<span data-ttu-id="04499-151"><> dimensione può essere un numero intero o un riferimento denominato a un altro membro del modello il cui valore viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="04499-151"><dimension-size> can either be an integer or a named reference to another template member whose value is then substituted.</span></span> <span data-ttu-id="04499-152">Le matrici possono essere di dimensione n, dove n è determinato dal numero di parentesi quadre abbinate che seguono l'istruzione, come nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="04499-152">Arrays can be n-dimensional, where n is determined by the number of paired square brackets trailing the statement, as in the following example.</span></span>


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a><span data-ttu-id="04499-153">Restrizioni del modello</span><span class="sxs-lookup"><span data-stu-id="04499-153">Template Restrictions</span></span>

<span data-ttu-id="04499-154">I modelli possono essere aperti, chiusi o limitati.</span><span class="sxs-lookup"><span data-stu-id="04499-154">Templates can be open, closed, or restricted.</span></span> <span data-ttu-id="04499-155">Queste restrizioni determinano i tipi di dati che possono essere visualizzati nella gerarchia immediata di un oggetto dati definito dal modello.</span><span class="sxs-lookup"><span data-stu-id="04499-155">These restrictions determine which data types can appear in the immediate hierarchy of a data object defined by the template.</span></span> <span data-ttu-id="04499-156">Un modello aperto non presenta alcuna restrizione, un modello chiuso rifiuta tutti i tipi di dati e un modello con restrizioni consente un elenco denominato di tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="04499-156">An open template has no restrictions, a closed template rejects all data types, and a restricted template allows a named list of data types.</span></span>

<span data-ttu-id="04499-157">La sintassi per indicare un modello aperto è di tre punti racchiusi tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="04499-157">The syntax for indicating an open template is three periods enclosed by square brackets.</span></span>


```
[ ... ]
```



<span data-ttu-id="04499-158">Un elenco delimitato da virgole di tipi di dati denominati seguiti facoltativamente da UUID racchiusi tra parentesi quadre indica un modello con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="04499-158">A comma-separated list of named data types followed optionally by their UUIDs enclosed by square brackets indicates a restricted template.</span></span>


```
[ { data-type [ UUID ] , } ... ]
```



<span data-ttu-id="04499-159">L'assenza di uno dei valori precedenti indica un modello chiuso.</span><span class="sxs-lookup"><span data-stu-id="04499-159">The absence of either of the above indicates a closed template.</span></span>

## <a name="template-example"></a><span data-ttu-id="04499-160">Esempio di modello</span><span class="sxs-lookup"><span data-stu-id="04499-160">Template Example</span></span>

<span data-ttu-id="04499-161">Di seguito viene illustrato un modello di esempio.</span><span class="sxs-lookup"><span data-stu-id="04499-161">The following shows an example template.</span></span>


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a><span data-ttu-id="04499-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04499-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04499-163">Codifica testo</span><span class="sxs-lookup"><span data-stu-id="04499-163">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



