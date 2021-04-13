---
description: 'Altre informazioni: colonne con tag, fisse e variabili'
title: Colonne con tag, fisse e variabili
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 3f27237c5f75874f7320f675affe20f3833084b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484869"
---
# <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="4655e-103">Colonne con tag, fisse e variabili</span><span class="sxs-lookup"><span data-stu-id="4655e-103">Tagged, Fixed and Variable Columns</span></span>


<span data-ttu-id="4655e-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4655e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="tagged-fixed-and-variable-columns"></a><span data-ttu-id="4655e-105">Colonne con tag, fisse e variabili</span><span class="sxs-lookup"><span data-stu-id="4655e-105">Tagged, Fixed and Variable Columns</span></span>

<span data-ttu-id="4655e-106">Le colonne con tag, a lunghezza fissa e a lunghezza variabile sono i tipi di colonna primari supportati da ESE.</span><span class="sxs-lookup"><span data-stu-id="4655e-106">Tagged, fixed, and variable-length columns are the primary column types supported by ESE.</span></span> <span data-ttu-id="4655e-107">Le colonne con tag non sono presenti in un record a meno che i dati non vengano archiviati nella colonna e possano essere a lunghezza fissa o variabile.</span><span class="sxs-lookup"><span data-stu-id="4655e-107">Tagged columns are not present in a record unless data is stored in the column, and may be fixed or variable length.</span></span> <span data-ttu-id="4655e-108">Le colonne con tag possono anche contenere più di un valore in un singolo record.</span><span class="sxs-lookup"><span data-stu-id="4655e-108">Tagged columns can also contain more than one value in a single record.</span></span> <span data-ttu-id="4655e-109">Le colonne fisse accettano la stessa quantità di spazio in ogni riga e richiedono 1 bit per rappresentare il valore NULL.</span><span class="sxs-lookup"><span data-stu-id="4655e-109">Fixed columns take the same amount of space in every row, and require 1 bit to represent the NULL value.</span></span> <span data-ttu-id="4655e-110">Le colonne a lunghezza variabile richiedono 2 byte per rappresentare le dimensioni e il valore NULL e occupano una quantità variabile di spazio in ogni record.</span><span class="sxs-lookup"><span data-stu-id="4655e-110">Variable length columns require 2 bytes to represent the size and NULL value, and occupy a variable amount of space in each record.</span></span> <span data-ttu-id="4655e-111">Per ulteriori informazioni sulle colonne contrassegnate e fisse, vedere il Jet_bitColumnTagged e Jet_bitColumnFixed opzione nel membro **grbit** della struttura [JET_COLUMNDEF](./jet-columndef-structure.md) utilizzata nella chiamata a [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="4655e-111">For more information on the tagged and fixed columns, see the Jet_bitColumnTagged, and Jet_bitColumnFixed option in the **grbit** member of [JET_COLUMNDEF](./jet-columndef-structure.md) structure used in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span>

<span data-ttu-id="4655e-112">Le colonne a lunghezza variabile sono determinate dal tipo di colonna impostato nel parametro *coltyp* nella chiamata a [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="4655e-112">Variable-length columns are determined by the column type that is set in the *coltyp* parameter in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="4655e-113">I tipi di colonna seguenti possono essere a lunghezza fissa o variabile a seconda che sia impostata l'opzione Jet_bitColumnFixed:</span><span class="sxs-lookup"><span data-stu-id="4655e-113">The following column types may be fixed or variable length depending on whether the Jet_bitColumnFixed option is set:</span></span>

  - <span data-ttu-id="4655e-114">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="4655e-114">JET_coltypBinary</span></span>

  - <span data-ttu-id="4655e-115">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="4655e-115">JET_coltypText</span></span>

  - <span data-ttu-id="4655e-116">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="4655e-116">JET_coltypLongBinary</span></span>

  - <span data-ttu-id="4655e-117">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="4655e-117">JET_coltypLongText</span></span>

<span data-ttu-id="4655e-118">In generale, i dati nel record vengono archiviati con l'intervallo fisso per primo, l'intervallo di variabili successivo e l'intervallo con tag archiviato per ultimo.</span><span class="sxs-lookup"><span data-stu-id="4655e-118">In general, data in the record is stored with the fixed range first, the variable range next, and the tagged range stored last.</span></span> <span data-ttu-id="4655e-119">Nel diagramma seguente viene illustrato il modo in cui i record vengono archiviati nella tabella.</span><span class="sxs-lookup"><span data-stu-id="4655e-119">The following diagram shows how the records are stored in the table.</span></span> <span data-ttu-id="4655e-120">Come illustrato nel diagramma, l'intervallo con tag può contenere colonne con più valori.</span><span class="sxs-lookup"><span data-stu-id="4655e-120">As shown in the diagram, the tagged range may contain columns with multiple values.</span></span>

<span data-ttu-id="4655e-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="4655e-121">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>
