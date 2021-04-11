---
description: ICE55 verifica che tutti gli oggetti LockPermission esistano e dispongano di valori di autorizzazione validi.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239093e3502a1731c3248918750c18aa1b3e1f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232856"
---
# <a name="ice55"></a><span data-ttu-id="40647-103">ICE55</span><span class="sxs-lookup"><span data-stu-id="40647-103">ICE55</span></span>

<span data-ttu-id="40647-104">ICE55 verifica che tutti gli oggetti LockPermission esistano e dispongano di valori di autorizzazione validi.</span><span class="sxs-lookup"><span data-stu-id="40647-104">ICE55 validates that all LockPermission objects exist and have valid permission values.</span></span>

## <a name="result"></a><span data-ttu-id="40647-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="40647-105">Result</span></span>

<span data-ttu-id="40647-106">ICE55 pubblica un errore se un LockObject elencato nella [tabella LockPermissions](lockpermissions-table.md) non esiste o se non è stato specificato alcun livello di privilegio nella colonna autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="40647-106">ICE55 post an error if a LockObject listed in the [LockPermissions table](lockpermissions-table.md) does not exist or if no privilege level is specified in the Permission column.</span></span>

## <a name="example"></a><span data-ttu-id="40647-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="40647-107">Example</span></span>

<span data-ttu-id="40647-108">ICE55 segnala gli errori seguenti per l'esempio.</span><span class="sxs-lookup"><span data-stu-id="40647-108">ICE55 would report the following errors for the example.</span></span>

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

<span data-ttu-id="40647-109">[Tabella LockPermissions](lockpermissions-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="40647-109">[LockPermissions Table](lockpermissions-table.md) (partial)</span></span>



| <span data-ttu-id="40647-110">LockObject</span><span class="sxs-lookup"><span data-stu-id="40647-110">LockObject</span></span> | <span data-ttu-id="40647-111">Tabella</span><span class="sxs-lookup"><span data-stu-id="40647-111">Table</span></span> | <span data-ttu-id="40647-112">Dominio</span><span class="sxs-lookup"><span data-stu-id="40647-112">Domain</span></span> | <span data-ttu-id="40647-113">User</span><span class="sxs-lookup"><span data-stu-id="40647-113">User</span></span>  | <span data-ttu-id="40647-114">Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="40647-114">Permission</span></span> |
|------------|-------|--------|-------|------------|
| <span data-ttu-id="40647-115">File1</span><span class="sxs-lookup"><span data-stu-id="40647-115">File1</span></span>      | <span data-ttu-id="40647-116">File</span><span class="sxs-lookup"><span data-stu-id="40647-116">File</span></span>  |        | <span data-ttu-id="40647-117">guest</span><span class="sxs-lookup"><span data-stu-id="40647-117">guest</span></span> |            |
| <span data-ttu-id="40647-118">File3</span><span class="sxs-lookup"><span data-stu-id="40647-118">File3</span></span>      | <span data-ttu-id="40647-119">File</span><span class="sxs-lookup"><span data-stu-id="40647-119">File</span></span>  |        | <span data-ttu-id="40647-120">guest</span><span class="sxs-lookup"><span data-stu-id="40647-120">guest</span></span> | <span data-ttu-id="40647-121">1</span><span class="sxs-lookup"><span data-stu-id="40647-121">1</span></span>          |



 

<span data-ttu-id="40647-122">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="40647-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="40647-123">File</span><span class="sxs-lookup"><span data-stu-id="40647-123">File</span></span>  | <span data-ttu-id="40647-124">Versione</span><span class="sxs-lookup"><span data-stu-id="40647-124">Version</span></span> | <span data-ttu-id="40647-125">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="40647-125">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="40647-126">File1</span><span class="sxs-lookup"><span data-stu-id="40647-126">File1</span></span> | <span data-ttu-id="40647-127">File2</span><span class="sxs-lookup"><span data-stu-id="40647-127">File2</span></span>   |          |
| <span data-ttu-id="40647-128">File2</span><span class="sxs-lookup"><span data-stu-id="40647-128">File2</span></span> | <span data-ttu-id="40647-129">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="40647-129">1.0.0.0</span></span> | <span data-ttu-id="40647-130">1033</span><span class="sxs-lookup"><span data-stu-id="40647-130">1033</span></span>     |



 

<span data-ttu-id="40647-131">L'oggetto file1 contiene un valore null nella colonna autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="40647-131">The object File1 has a null in the Permission column.</span></span> <span data-ttu-id="40647-132">Ogni riga deve avere un valore nella colonna autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="40647-132">Each row must have a value in the Permissions column.</span></span> <span data-ttu-id="40647-133">Per correggere l'errore, specificare un valore numerico in questa colonna.</span><span class="sxs-lookup"><span data-stu-id="40647-133">To fix this error specify a numeric value in this column.</span></span> <span data-ttu-id="40647-134">Se non sono necessari privilegi per questo oggetto, è necessario rimuovere la riga.</span><span class="sxs-lookup"><span data-stu-id="40647-134">If no privileges are needed for this object then you should remove the row.</span></span>

<span data-ttu-id="40647-135">L'oggetto file3 descritto nella tabella LockPermissions non è elencato nella tabella file.</span><span class="sxs-lookup"><span data-stu-id="40647-135">The object File3 described in the LockPermissions table is not listed in the File table.</span></span> <span data-ttu-id="40647-136">Per correggere l'errore, fare riferimento a un oggetto valido.</span><span class="sxs-lookup"><span data-stu-id="40647-136">To fix this error refer to a valid object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40647-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40647-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40647-138">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="40647-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



