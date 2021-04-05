---
description: "I tipi di dati seguenti sono definiti nell'API copia shadow del volume:"
ms.assetid: e64b36d6-4f10-42bd-9ad4-00aba90e9715
title: Tipi di dati dell'API copia shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99717bc87a59ee03cb93ef7f6abbdf429e3d3bec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751583"
---
# <a name="volume-shadow-copy-api-data-types"></a><span data-ttu-id="3b48e-103">Tipi di dati dell'API copia shadow del volume</span><span class="sxs-lookup"><span data-stu-id="3b48e-103">Volume Shadow Copy API Data Types</span></span>

<span data-ttu-id="3b48e-104">I tipi di dati seguenti sono definiti nell'API copia shadow del volume:</span><span class="sxs-lookup"><span data-stu-id="3b48e-104">The following data types are defined in the Volume Shadow Copy API:</span></span>

<dl> <dt>

<span data-ttu-id="3b48e-105"><span id="VSS_ID"></span><span id="vss_id"></span>\_ID VSS</span><span class="sxs-lookup"><span data-stu-id="3b48e-105"><span id="VSS_ID"></span><span id="vss_id"></span>VSS\_ID</span></span>
</dt> <dd>

``` syntax
typedef GUID VSS_ID;
```

<span data-ttu-id="3b48e-106">La definizione dell' **\_ ID VSS** specifica il formato generale dell'identificatore VSS.</span><span class="sxs-lookup"><span data-stu-id="3b48e-106">The **VSS\_ID** definition specifies the general VSS identifier format.</span></span> <span data-ttu-id="3b48e-107">L' **\_ ID VSS** è un tipo di dati GUID standard.</span><span class="sxs-lookup"><span data-stu-id="3b48e-107">The **VSS\_ID** is a standard GUID data type.</span></span>

<span data-ttu-id="3b48e-108">Servizio Copia **shadow \_ del volume Gli ID** vengono utilizzati per identificare gli elementi seguenti: copie shadow, set di copie shadow, provider, versioni del provider, Writer (identificatore di classe del writer) e istanze di writer.</span><span class="sxs-lookup"><span data-stu-id="3b48e-108">**VSS\_ID** s are used to identify the following: shadow copies, shadow copy sets, providers, provider versions, writers (writer's class identifier), and instances of writers.</span></span>

</dd> <dt>

<span data-ttu-id="3b48e-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>\_PWSZ VSS</span><span class="sxs-lookup"><span data-stu-id="3b48e-109"><span id="VSS_PWSZ"></span><span id="vss_pwsz"></span>VSS\_PWSZ</span></span>
</dt> <dd>

``` syntax
typedef /* [string][unique] */  __RPC_unique_pointer  __RPC_string WCHAR *VSS_PWSZ;
```

<span data-ttu-id="3b48e-110">La definizione **VSS \_ PWSZ** specifica una stringa di caratteri wide a terminazione null (WCHAR).</span><span class="sxs-lookup"><span data-stu-id="3b48e-110">The **VSS\_PWSZ** definition specifies a null-terminated wide character string (wchar).</span></span>

</dd> <dt>

<span data-ttu-id="3b48e-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>\_timestamp VSS</span><span class="sxs-lookup"><span data-stu-id="3b48e-111"><span id="VSS_TIMESTAMP"></span><span id="vss_timestamp"></span>VSS\_TIMESTAMP</span></span>
</dt> <dd>

``` syntax
typedef LONGLONG VSS_TIMESTAMP;
```

<span data-ttu-id="3b48e-112">La definizione del **\_ timestamp VSS** contiene informazioni timestamp come valore integer a 64 bit contenente il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="3b48e-112">The **VSS\_TIMESTAMP** definition holds time-stamp information as a 64-bit integer value containing the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="3b48e-113">Questa definizione è interscambiabile con la struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="3b48e-113">This definition is interchangeable with the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> </dl>

 

 
