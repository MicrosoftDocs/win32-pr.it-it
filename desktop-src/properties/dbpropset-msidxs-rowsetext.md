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
# <a name="dbpropset_msidxs_rowsetext"></a>DBPROPSET \_ MSIDXS \_ ROWSETEXT

Estende le proprietà definite per le API del set di righe.

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

Il \_ set di proprietà DBPROPSET MSIDXS \_ ROWSETEXT contiene le costanti di proprietà seguenti:

<dl> <dt>

<span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>\_ROWSETQUERYSTATUS MSIDXSPROP
</dt> <dd>

ID proprietà 2. Stato della query per il set di righe. Le \_ \* costanti stat indicano lo stato di esecuzione e di affidabilità.

</dd> <dt>

<span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>\_stringa delle \_ impostazioni locali del comando MSIDXSPROP \_
</dt> <dd>

ID proprietà 3. Stringa delle impostazioni locali che rappresenta le impostazioni locali e della lingua da utilizzare per questo set di righe.

</dd> <dt>

<span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>\_ \_ restrizione query MSIDXSPROP
</dt> <dd>

ID proprietà 4. Stringa di query associata a questo set di righe.

</dd> <dt>

<span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>\_albero di analisi MSIDXSPROP \_
</dt> <dd>

ID proprietà 5.

</dd> <dt>

<span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>\_rango massimo \_ MSIDXSPROP 
</dt> <dd>

ID proprietà 6.

</dd> <dt>

<span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>risultati di MSIDXSPROP \_ \_ trovati
</dt> <dd>

ID proprietà 7.

</dd> <dt>

<span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>\_WHEREID MSIDXSPROP
</dt> <dd>

ID proprietà 8.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>\_versione del server MSIDXSPROP \_ 
</dt> <dd>

Novità di Windows 7. ID proprietà 9. Versione del server.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>\_Server MSIDXSPROP \_ winver \_ Major
</dt> <dd>

ID proprietà 10.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP \_ server \_ winver \_ minor
</dt> <dd>

ID proprietà 11.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>\_NLSVERSION server \_ MSIDXSPROP
</dt> <dd>

ID proprietà 12.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>\_NLSVER del server MSIDXSPROP \_ \_ definito 
</dt> <dd>

ID proprietà 13.

</dd> <dt>

<span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP \_ stesso \_ SORTORDER \_ usato 
</dt> <dd>

ID proprietà 14.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per eseguire una \_ query \_ sulla versione del server MSIDXSPROP, è necessario eseguire la query fittizia sul server, ad esempio l'esempio seguente.

`SELECT top 1 workid from servername.systemindex`

Dopo che il set di righe è stato restituito, chiamare [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per le funzionalità del set di righe e quindi chiamare [IRowsetInfo:: GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) per la nuova proprietà ( \_ versione del server MSIDXSPROP \_ ). Il tipo della proprietà è **VT \_ I4** . i possibili valori sono i seguenti:

\#definire la \_ versione ci \_ WDS30 0x102//258

\#definire la \_ versione ci \_ WDS40 0x109//265

\#definire la \_ versione ci \_ WIN70 0x700//1792

Una volta che il valore è noto, il client può formare una query supportata dal server ed emettere una query reale.

DBPROPSET \_ MSIDXS \_ ROWSETEXT è dichiarata in NTQuery. h.

 

 
