---
title: Marshalling utente
description: Marshalling utente in RPC (Remote Procedure Call).
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c901fd8c75137b4657322a89692ff8a3afb5408
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856141"
---
# <a name="user-marshal"></a><span data-ttu-id="3b2ca-103">Marshalling utente</span><span class="sxs-lookup"><span data-stu-id="3b2ca-103">User-marshal</span></span>

<span data-ttu-id="3b2ca-104">Il marshalling dell'utente ha una stringa di formato simile a trasmissione \_ come:</span><span class="sxs-lookup"><span data-stu-id="3b2ca-104">User marshal has a format string that is similar to transmit\_as:</span></span>

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

<span data-ttu-id="3b2ca-105">I flag<1> byte sono costituiti dal contrassegno superiore e dal bocconcino di allineamento inferiore.</span><span class="sxs-lookup"><span data-stu-id="3b2ca-105">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="3b2ca-106">I 2 bit superiori del contrassegno sono usati per descrivere se il tipo di Wire è definito come puntatore univoco, puntatore di riferimento o nessun puntatore (non può essere un PTR).</span><span class="sxs-lookup"><span data-stu-id="3b2ca-106">The upper 2 bits of the flag nibble are used to describe whether the wire type is defined as a unique pointer, reference pointer or no pointer (it cannot be a ptr).</span></span> <span data-ttu-id="3b2ca-107">Per impostare o ottenere i flag, sono stati definiti i manifesti seguenti:</span><span class="sxs-lookup"><span data-stu-id="3b2ca-107">The following manifests have been defined to set/get the flags:</span></span>

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

<span data-ttu-id="3b2ca-108">Il bocconcino di allineamento della parola del flag mantiene l'allineamento del conduttore del tipo trasmesso.</span><span class="sxs-lookup"><span data-stu-id="3b2ca-108">The alignment nibble of the flag word keeps the wire alignment of the transmitted type.</span></span>

<span data-ttu-id="3b2ca-109">L'indice quadruplo \_<2> è un indice della routine di callback quadrupla delle funzioni di marshalling degli utenti.</span><span class="sxs-lookup"><span data-stu-id="3b2ca-109">The quadruple\_index<2> is an index of the callback routine quadruple of the user marshal functions.</span></span> <span data-ttu-id="3b2ca-110">Le posizioni di routine sono le seguenti: ridimensionamento, marshalling, unmarshalling e liberazione di routine.</span><span class="sxs-lookup"><span data-stu-id="3b2ca-110">The routine positions are as follow: sizing, marshaling, unmarshaling, and freeing routine.</span></span>

<span data-ttu-id="3b2ca-111">La \_ dimensione della memoria del tipo di utente \_ \_<2> fornisce una dimensione per il tipo specifico dell'utente, inclusi i tipi sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="3b2ca-111">The user\_type\_memory\_size<2> provides a size for the user specific type, including unknown types.</span></span>

<span data-ttu-id="3b2ca-112">Le \_ dimensioni del buffer dei tipi trasmessi \_ \_<2> sono pari a zero quando la dimensione è variabile o alle dimensioni fisse effettive.</span><span class="sxs-lookup"><span data-stu-id="3b2ca-112">The transmitted\_type\_buffer\_size<2> is either zero when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="3b2ca-113">Si tratta di un'ottimizzazione che consente a MIDL di ignorare i callback durante il ridimensionamento del buffer e anche quando viene liberato.</span><span class="sxs-lookup"><span data-stu-id="3b2ca-113">This is an optimization that enables MIDL to skip callbacks when sizing the buffer, and also when freeing.</span></span>

## <a name="range"></a><span data-ttu-id="3b2ca-114">Range</span><span class="sxs-lookup"><span data-stu-id="3b2ca-114">Range</span></span>

<span data-ttu-id="3b2ca-115">Il \[ controllo dell'intervallo \] fornisce metodi aggiuntivi per la convalida degli argomenti a livello di rapporto di recapito.</span><span class="sxs-lookup"><span data-stu-id="3b2ca-115">The \[range\] checking provides additional means for argument validation at the NDR layer.</span></span> <span data-ttu-id="3b2ca-116">Il \[ \] descrittore di intervallo presenta il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="3b2ca-116">The \[range\] descriptor has the following format:</span></span>

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

<span data-ttu-id="3b2ca-117">I flag accettano il bocconcino superiore e il tipo il bocconcino inferiore del secondo byte.</span><span class="sxs-lookup"><span data-stu-id="3b2ca-117">The flags take the upper nibble and the type the lower nibble of the second byte.</span></span> <span data-ttu-id="3b2ca-118">I valori bassi e alti dipendono dal tipo della variabile da verificare.</span><span class="sxs-lookup"><span data-stu-id="3b2ca-118">The low and high values depend on the type of the variable to be checked.</span></span>

<span data-ttu-id="3b2ca-119">I flag sono intesi come veicoli di espansione. il compilatore ha impostato il bocconcino su zero.</span><span class="sxs-lookup"><span data-stu-id="3b2ca-119">The flags are meant as an expansion vehicle; the compiler has been setting the nibble to zero.</span></span>

 

 




