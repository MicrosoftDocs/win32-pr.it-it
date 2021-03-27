---
title: Tipo definito dall'utente
description: Utilizzare la sintassi seguente per dichiarare un tipo definito dall'utente.
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2107e3eb2b2dc2362776a1a9ecd50830519c6627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395575"
---
# <a name="user-defined-type"></a><span data-ttu-id="06107-103">Tipo definito dall'utente</span><span class="sxs-lookup"><span data-stu-id="06107-103">User-Defined Type</span></span>

<span data-ttu-id="06107-104">Utilizzare la sintassi seguente per dichiarare un tipo definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="06107-104">Use the following syntax to declare a user-defined type.</span></span>



|                                           |
|-------------------------------------------|
| <span data-ttu-id="06107-105">**\[ \] \[ indice \] del nome di tipo const** di typedef;</span><span class="sxs-lookup"><span data-stu-id="06107-105">typedef **\[const\] Type Name\[Index\]**;</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="06107-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="06107-106">Parameters</span></span>



| <span data-ttu-id="06107-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="06107-107">Item</span></span>                                                                                         | <span data-ttu-id="06107-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06107-108">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06107-109"><span id="_const_"></span><span id="_CONST_"></span>**\[const\]**</span><span class="sxs-lookup"><span data-stu-id="06107-109"><span id="_const_"></span><span id="_CONST_"></span>**\[const\]**</span></span><br/>                 | <span data-ttu-id="06107-110">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="06107-110">Optional.</span></span> <span data-ttu-id="06107-111">Questa parola chiave contrassegna in modo esplicito il tipo come costante.</span><span class="sxs-lookup"><span data-stu-id="06107-111">This keyword explicitly marks the type as a constant.</span></span><br/>             |
| <span data-ttu-id="06107-112"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Tipo**</span><span class="sxs-lookup"><span data-stu-id="06107-112"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/>     | <span data-ttu-id="06107-113">Identifica il tipo di dati. deve essere uno dei tipi di dati intrinseci HLSL.</span><span class="sxs-lookup"><span data-stu-id="06107-113">Identifies the data type; must be one of the HLSL intrinsic data types.</span></span><br/>     |
| <span data-ttu-id="06107-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**</span><span class="sxs-lookup"><span data-stu-id="06107-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="06107-115">Stringa ASCII che identifica in modo univoco il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="06107-115">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="06107-116"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Indice**</span><span class="sxs-lookup"><span data-stu-id="06107-116"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Index**</span></span><br/> | <span data-ttu-id="06107-117">Dimensioni della matrice facoltative.</span><span class="sxs-lookup"><span data-stu-id="06107-117">Optional array size.</span></span> <span data-ttu-id="06107-118">Deve essere un Unsigned Integer compreso tra 1 e 4 inclusi.</span><span class="sxs-lookup"><span data-stu-id="06107-118">Must be an unsigned integer between 1 and 4 inclusive.</span></span><br/> |



 

<span data-ttu-id="06107-119">Oltre ai tipi di dati intrinseci incorporati, HLSL supporta i tipi definiti dall'utente o personalizzati che seguono questa sintassi:</span><span class="sxs-lookup"><span data-stu-id="06107-119">In addition to the built-in intrinsic data types, HLSL supports user-defined or custom types which follow this syntax:</span></span>

## <a name="remarks"></a><span data-ttu-id="06107-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="06107-120">Remarks</span></span>

<span data-ttu-id="06107-121">I tipi definiti dall'utente non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="06107-121">User-defined types are not case-sensitive.</span></span> <span data-ttu-id="06107-122">Per praticità, i tipi seguenti vengono definiti automaticamente in ambito super-globale.</span><span class="sxs-lookup"><span data-stu-id="06107-122">For convenience, the following types are automatically defined at super-global scope.</span></span>


```
typedef vector <bool, #> bool#;
typedef vector <int, #> int#;
typedef vector <uint, #> uint#;
typedef vector <half, #> half#;
typedef vector <float, #> float#;
typedef vector <double, #> double#;

typedef matrix <bool, #, #> bool#x#;
typedef matrix <int, #, #> int#x#;
typedef matrix <uint, #, #> uint#x#;
typedef matrix <half, #, #> half#x#;
typedef matrix <float, #, #> float#x#;
typedef matrix <double, #, #> double#x#;
```



<span data-ttu-id="06107-123">Il segno di cancelletto ( \# ) rappresenta una cifra intera compresa tra 1 e 4.</span><span class="sxs-lookup"><span data-stu-id="06107-123">The pound sign (\#) represents an integer digit between 1 and 4.</span></span>

<span data-ttu-id="06107-124">Per la compatibilità con gli effetti di DirectX 8, i tipi seguenti vengono definiti automaticamente in ambito super-globale:</span><span class="sxs-lookup"><span data-stu-id="06107-124">For compatibility with DirectX 8 effects, the following types are automatically defined at super-global scope:</span></span>


```
typedef int DWORD;
typedef float FLOAT; 
typedef vector <float, 4> VECTOR;
typedef matrix <float, 4, 4> MATRIX;
typedef string STRING;
typedef texture TEXTURE;
typedef pixelshader PIXELSHADER;
typedef vertexshader VERTEXSHADER;
```



## <a name="related-topics"></a><span data-ttu-id="06107-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06107-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06107-126">Tipi di dati (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06107-126">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





