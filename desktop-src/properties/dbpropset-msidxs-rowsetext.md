---
description: Estende le proprietà definite per le API del set di righe.
ms.assetid: C1A2DF19-C68D-42CC-9CB2-190F22CB4158
title: DBPROPSET_MSIDXS_ROWSETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba37466c52f2fa9f83e3aa439ace03c1fba34f44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316413"
---
# <a name="dbpropset_msidxs_rowsetext"></a><span data-ttu-id="ca4a9-103">DBPROPSET \_ MSIDXS \_ ROWSETEXT</span><span class="sxs-lookup"><span data-stu-id="ca4a9-103">DBPROPSET\_MSIDXS\_ROWSETEXT</span></span>

<span data-ttu-id="ca4a9-104">Estende le proprietà definite per le API del set di righe.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-104">Extends properties defined for the Rowset APIs.</span></span>

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

<span data-ttu-id="ca4a9-105">Il \_ set di proprietà DBPROPSET MSIDXS \_ ROWSETEXT contiene le costanti di proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="ca4a9-105">The DBPROPSET\_MSIDXS\_ROWSETEXT property set contains the following property constants:</span></span>

<dl> <dt>

<span data-ttu-id="ca4a9-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>\_ROWSETQUERYSTATUS MSIDXSPROP</span><span class="sxs-lookup"><span data-stu-id="ca4a9-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP\_ROWSETQUERYSTATUS</span></span>
</dt> <dd>

<span data-ttu-id="ca4a9-107">ID proprietà 2.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-107">Property ID 2.</span></span> <span data-ttu-id="ca4a9-108">Stato della query per il set di righe.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-108">Query status for the rowset.</span></span> <span data-ttu-id="ca4a9-109">Le \_ \* costanti stat indicano lo stato di esecuzione e di affidabilità.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-109">The STAT\_\* constants indicate the execution and reliability status.</span></span>

</dd> <dt>

<span data-ttu-id="ca4a9-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>\_stringa delle \_ impostazioni locali del comando MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="ca4a9-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>MSIDXSPROP\_COMMAND\_LOCALE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="ca4a9-111">ID proprietà 3.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-111">Property ID 3.</span></span> <span data-ttu-id="ca4a9-112">Stringa delle impostazioni locali che rappresenta le impostazioni locali e della lingua da utilizzare per questo set di righe.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-112">Locale string that represents the language and locale setting to use for this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="ca4a9-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>\_ \_ restrizione query MSIDXSPROP</span><span class="sxs-lookup"><span data-stu-id="ca4a9-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>MSIDXSPROP\_QUERY\_RESTRICTION</span></span>
</dt> <dd>

<span data-ttu-id="ca4a9-114">ID proprietà 4.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-114">Property ID 4.</span></span> <span data-ttu-id="ca4a9-115">Stringa di query associata a questo set di righe.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-115">The query string associated with this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="ca4a9-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>\_albero di analisi MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="ca4a9-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>MSIDXSPROP\_PARSE\_TREE</span></span>
</dt> <dd>

<span data-ttu-id="ca4a9-117">ID proprietà 5.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-117">Property ID 5.</span></span>

</dd> <dt>

<span data-ttu-id="ca4a9-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>\_rango massimo \_ MSIDXSPROP</span><span class="sxs-lookup"><span data-stu-id="ca4a9-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>MSIDXSPROP\_MAX\_RANK</span></span> 
</dt> <dd>

<span data-ttu-id="ca4a9-119">ID proprietà 6.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-119">Property ID 6.</span></span>

</dd> <dt>

<span data-ttu-id="ca4a9-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>risultati di MSIDXSPROP \_ \_ trovati</span><span class="sxs-lookup"><span data-stu-id="ca4a9-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>MSIDXSPROP\_RESULTS\_FOUND</span></span>
</dt> <dd>

<span data-ttu-id="ca4a9-121">ID proprietà 7.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-121">Property ID 7.</span></span>

</dd> <dt>

<span data-ttu-id="ca4a9-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>\_WHEREID MSIDXSPROP</span><span class="sxs-lookup"><span data-stu-id="ca4a9-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP\_WHEREID</span></span>
</dt> <dd>

<span data-ttu-id="ca4a9-123">ID proprietà 8.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-123">Property ID 8.</span></span>

</dd> <dt>

<span data-ttu-id="ca4a9-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>\_versione del server MSIDXSPROP \_</span><span class="sxs-lookup"><span data-stu-id="ca4a9-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>MSIDXSPROP\_SERVER\_VERSION</span></span> 
</dt> <dd>

<span data-ttu-id="ca4a9-125">Novità di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-125">New for Windows 7.</span></span> <span data-ttu-id="ca4a9-126">ID proprietà 9.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-126">Property ID 9.</span></span> <span data-ttu-id="ca4a9-127">Versione del server.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-127">The server version.</span></span>

</dd> <dt>

<span data-ttu-id="ca4a9-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>\_Server MSIDXSPROP \_ winver \_ Major</span><span class="sxs-lookup"><span data-stu-id="ca4a9-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP\_SERVER\_WINVER\_MAJOR</span></span>
</dt> <dd>

<span data-ttu-id="ca4a9-129">ID proprietà 10.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-129">Property ID 10.</span></span>

</dd> <dt>

<span data-ttu-id="ca4a9-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP \_ server \_ winver \_ minor</span><span class="sxs-lookup"><span data-stu-id="ca4a9-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP\_SERVER\_WINVER\_MINOR</span></span>
</dt> <dd>

<span data-ttu-id="ca4a9-131">ID proprietà 11.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-131">Property ID 11.</span></span>

</dd> <dt>

<span data-ttu-id="ca4a9-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>\_NLSVERSION server \_ MSIDXSPROP</span><span class="sxs-lookup"><span data-stu-id="ca4a9-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP\_SERVER\_NLSVERSION</span></span>
</dt> <dd>

<span data-ttu-id="ca4a9-133">ID proprietà 12.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-133">Property ID 12.</span></span>

</dd> <dt>

<span data-ttu-id="ca4a9-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>\_NLSVER del server MSIDXSPROP \_ \_ definito</span><span class="sxs-lookup"><span data-stu-id="ca4a9-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP\_SERVER\_NLSVER\_DEFINED</span></span> 
</dt> <dd>

<span data-ttu-id="ca4a9-135">ID proprietà 13.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-135">Property ID 13.</span></span>

</dd> <dt>

<span data-ttu-id="ca4a9-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP \_ stesso \_ SORTORDER \_ usato</span><span class="sxs-lookup"><span data-stu-id="ca4a9-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP\_SAME\_SORTORDER\_USED</span></span> 
</dt> <dd>

<span data-ttu-id="ca4a9-137">ID proprietà 14.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-137">Property ID 14.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca4a9-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca4a9-138">Remarks</span></span>

<span data-ttu-id="ca4a9-139">Per eseguire una \_ query \_ sulla versione del server MSIDXSPROP, è necessario eseguire la query fittizia sul server, ad esempio l'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-139">To query MSIDXSPROP\_SERVER\_VERSION, it is necessary to issue the dummy query to server, such as the following example.</span></span>

`SELECT top 1 workid from servername.systemindex`

<span data-ttu-id="ca4a9-140">Dopo che il set di righe è stato restituito, chiamare [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per le funzionalità del set di righe e quindi chiamare [IRowsetInfo:: GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) per la nuova proprietà ( \_ versione del server MSIDXSPROP \_ ).</span><span class="sxs-lookup"><span data-stu-id="ca4a9-140">After the rowset has been returned, call [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the capabilities of the rowset and then call [IRowsetInfo::GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) for the new property (MSIDXSPROP\_SERVER\_VERSION).</span></span> <span data-ttu-id="ca4a9-141">Il tipo della proprietà è **VT \_ I4** . i possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ca4a9-141">The property has a type of **VT\_I4** and can be one of the following values:</span></span>

<span data-ttu-id="ca4a9-142">\#definire la \_ versione ci \_ WDS30 0x102//258</span><span class="sxs-lookup"><span data-stu-id="ca4a9-142">\#define CI\_VERSION\_WDS30 0x102 // 258</span></span>

<span data-ttu-id="ca4a9-143">\#definire la \_ versione ci \_ WDS40 0x109//265</span><span class="sxs-lookup"><span data-stu-id="ca4a9-143">\#define CI\_VERSION\_WDS40 0x109 // 265</span></span>

<span data-ttu-id="ca4a9-144">\#definire la \_ versione ci \_ WIN70 0x700//1792</span><span class="sxs-lookup"><span data-stu-id="ca4a9-144">\#define CI\_VERSION\_WIN70 0x700 // 1792</span></span>

<span data-ttu-id="ca4a9-145">Una volta che il valore è noto, il client può formare una query supportata dal server ed emettere una query reale.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-145">Once the value is known, the client can form a query which is supported by the server and issue a real query.</span></span>

<span data-ttu-id="ca4a9-146">DBPROPSET \_ MSIDXS \_ ROWSETEXT è dichiarata in NTQuery. h.</span><span class="sxs-lookup"><span data-stu-id="ca4a9-146">DBPROPSET\_MSIDXS\_ROWSETEXT is declared in ntquery.h.</span></span>

 

 
