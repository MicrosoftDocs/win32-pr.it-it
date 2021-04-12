---
description: ICE98 verifica il campo della descrizione della tabella ODBCDataSource per un'origine dati ODBC. Usa la funzione SQLValidDSN per verificare che vengano usati solo caratteri validi e che la descrizione non superi la lunghezza massima consentita.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf06e97341bd8f15502b1ea1fe43a975dc9cde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232072"
---
# <a name="ice98"></a><span data-ttu-id="4641b-104">ICE98</span><span class="sxs-lookup"><span data-stu-id="4641b-104">ICE98</span></span>

<span data-ttu-id="4641b-105">ICE98 verifica il campo della descrizione della [tabella ODBCDataSource](odbcdatasource-table.md) per un'origine dati ODBC.</span><span class="sxs-lookup"><span data-stu-id="4641b-105">ICE98 verifies the description field of the [ODBCDataSource Table](odbcdatasource-table.md) for an ODBC data source.</span></span> <span data-ttu-id="4641b-106">Usa la funzione **SQLValidDSN** per verificare che vengano usati solo caratteri validi e che la descrizione non superi la lunghezza massima consentita.</span><span class="sxs-lookup"><span data-stu-id="4641b-106">It uses the **SQLValidDSN** function to check that only valid characters are used, and that the description does not exceed the maximum allowed length.</span></span>

## <a name="result"></a><span data-ttu-id="4641b-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="4641b-107">Result</span></span>

<span data-ttu-id="4641b-108">ICE98 invia gli avvisi seguenti.</span><span class="sxs-lookup"><span data-stu-id="4641b-108">ICE98 posts the following warnings.</span></span>



| <span data-ttu-id="4641b-109">Avviso di ICE98</span><span class="sxs-lookup"><span data-stu-id="4641b-109">ICE98 warning</span></span>                    | <span data-ttu-id="4641b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4641b-110">Description</span></span>                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4641b-111">Il nome dell'origine dati non è valido.</span><span class="sxs-lookup"><span data-stu-id="4641b-111">The data source name is invalid.</span></span> | <span data-ttu-id="4641b-112">Il valore nella colonna Descrizione della [tabella ODBCDataSource](odbcdatasource-table.md) contiene caratteri non validi o è troppo lungo, il che significa che supera la \_ lunghezza massima del \_ DSN SQL \_ di 32.</span><span class="sxs-lookup"><span data-stu-id="4641b-112">The value in the Description column of the [ODBCDataSource Table](odbcdatasource-table.md) either contains invalid characters or is too long, which means that it exceeds the SQL\_MAX\_DSN\_LENGTH of 32.</span></span> |



 

## <a name="example"></a><span data-ttu-id="4641b-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="4641b-113">Example</span></span>

<span data-ttu-id="4641b-114">ICE98 segnala gli avvisi seguenti per l'esempio:</span><span class="sxs-lookup"><span data-stu-id="4641b-114">ICE98 reports the following warnings for the example:</span></span>

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

<span data-ttu-id="4641b-115">[Tabella ODBCDataSource](odbcdatasource-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="4641b-115">[ODBCDataSource Table](odbcdatasource-table.md) (partial)</span></span>



| <span data-ttu-id="4641b-116">DataSource</span><span class="sxs-lookup"><span data-stu-id="4641b-116">DataSource</span></span> | <span data-ttu-id="4641b-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4641b-117">Description</span></span>                      |
|------------|----------------------------------|
| <span data-ttu-id="4641b-118">BadChar</span><span class="sxs-lookup"><span data-stu-id="4641b-118">BadChar</span></span>    | <span data-ttu-id="4641b-119">!</span><span class="sxs-lookup"><span data-stu-id="4641b-119">!</span></span>                                |
| <span data-ttu-id="4641b-120">TooLong</span><span class="sxs-lookup"><span data-stu-id="4641b-120">TooLong</span></span>    | <span data-ttu-id="4641b-121"><String of length > 32></span><span class="sxs-lookup"><span data-stu-id="4641b-121"><String of length > 32></span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4641b-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4641b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4641b-123">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="4641b-123">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="4641b-124">Tabella ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="4641b-124">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
</dt> </dl>

 

 



