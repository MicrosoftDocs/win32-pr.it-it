---
title: Il file di intestazione
description: Il file di intestazione contiene le definizioni di tutti i tipi di dati e le operazioni dichiarate nel file IDL, nonché tutti i tipi di dati e le operazioni dichiarati nei file inclusi con la direttiva \ include.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL e RPC MIDL, interfacce, file di intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61331d8bb72d322987c13d02b04632c95424e755
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045049"
---
# <a name="the-header-file"></a><span data-ttu-id="a87e2-104">Il file di intestazione</span><span class="sxs-lookup"><span data-stu-id="a87e2-104">The Header File</span></span>

<span data-ttu-id="a87e2-105">Il file di intestazione contiene le definizioni di tutti i tipi di dati e le operazioni dichiarate nel file IDL, nonché tutti i tipi di dati e le operazioni dichiarati nei file inclusi con la \# direttiva include.</span><span class="sxs-lookup"><span data-stu-id="a87e2-105">The header file contains definitions of all data types and operations declared in the IDL file, as well as all data types and operations declared in the files included with the \#include directive.</span></span> <span data-ttu-id="a87e2-106">I tipi di dati dei file importati con la direttiva Import non vengono replicati nel file di intestazione. il file di intestazione generato contiene invece una riga di inclusione per il file H generato dal file importato.</span><span class="sxs-lookup"><span data-stu-id="a87e2-106">Data types from the files imported with the import directive are not replicated to the header file; instead the generated header file contains an include line to the H file generated from the imported file.</span></span> <span data-ttu-id="a87e2-107">Il file di intestazione deve essere incluso in tutti i moduli dell'applicazione che chiamano le operazioni definite, implementano le operazioni definite o modificano i tipi definiti.</span><span class="sxs-lookup"><span data-stu-id="a87e2-107">The header file must be included by all application modules that call the defined operations, implement the defined operations, or manipulate the defined types.</span></span>

<span data-ttu-id="a87e2-108">Il compilatore MIDL passa [**/header**](-header.md) e [**/out**](-out.md) influisce sul file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="a87e2-108">The MIDL compiler switches [**/header**](-header.md) and [**/out**](-out.md) affect the header file.</span></span>

 

 




