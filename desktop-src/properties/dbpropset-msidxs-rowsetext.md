---
description: Estende le proprietà definite per le API del set di righe.
ms.assetid: C1A2DF19-C68D-42CC-9CB2-190F22CB4158
title: DBPROPSET_MSIDXS_ROWSETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8c647d4b1ecbf9e5cc88ccae4af649c27093472456377e478ff80f7a76f3a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776411"
---
# <a name="dbpropset_msidxs_rowsetext"></a>DBPROPSET \_ MSIDXS \_ ROWSETEXT

Estende le proprietà definite per le API del set di righe.

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

Il set di proprietà \_ DBPROPSET MSIDXS \_ ROWSETEXT contiene le costanti di proprietà seguenti:

<dl> <dt>

<span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP \_ ROWSETQUERYSTATUS
</dt> <dd>

ID proprietà 2. Stato della query per il set di righe. Le costanti STAT \_ \* indicano lo stato di esecuzione e affidabilità.

</dd> <dt>

<span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>STRINGA DELLE IMPOSTAZIONI LOCALI DEL COMANDO MSIDXSPROP \_ \_ \_
</dt> <dd>

ID proprietà 3. Stringa delle impostazioni locali che rappresenta la lingua e le impostazioni locali da utilizzare per questo set di righe.

</dd> <dt>

<span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>RESTRIZIONE DELLE QUERY MSIDXSPROP \_ \_
</dt> <dd>

ID proprietà 4. Stringa di query associata a questo set di righe.

</dd> <dt>

<span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>ALBERO DI ANALISI MSIDXSPROP \_ \_
</dt> <dd>

ID proprietà 5.

</dd> <dt>

<span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>MSIDXSPROP \_ MAX \_ RANK 
</dt> <dd>

ID proprietà 6.

</dd> <dt>

<span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>RISULTATI MSIDXSPROP \_ \_ TROVATI
</dt> <dd>

ID proprietà 7.

</dd> <dt>

<span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP \_ WHEREID
</dt> <dd>

ID proprietà 8.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>VERSIONE DEL SERVER MSIDXSPROP \_ \_ 
</dt> <dd>

Novità per Windows 7. ID proprietà 9. Versione del server.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP \_ SERVER \_ WINVER \_ MAJOR
</dt> <dd>

ID proprietà 10.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP \_ SERVER \_ WINVER \_ MINOR
</dt> <dd>

ID proprietà 11.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP \_ SERVER \_ NLSVERSION
</dt> <dd>

ID proprietà 12.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP \_ SERVER \_ NLSVER \_ DEFINITO 
</dt> <dd>

ID proprietà 13.

</dd> <dt>

<span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP \_ STESSO \_ ORDINAMENTO \_ USATO 
</dt> <dd>

ID proprietà 14.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per eseguire query su MSIDXSPROP SERVER VERSION, è necessario eseguire la query fittizia al server, ad esempio \_ \_ l'esempio seguente.

`SELECT top 1 workid from servername.systemindex`

Dopo aver restituito il set di righe, chiamare [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per le funzionalità del set di righe e quindi chiamare [IRowsetInfo::GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) per la nuova proprietà (MSIDXSPROP \_ SERVER \_ VERSION). La proprietà ha un tipo **VT \_ I4** e può essere uno dei valori seguenti:

\#definire LA \_ VERSIONE \_ CI WDS30 0x102 // 258

\#definire LA \_ VERSIONE \_ CI WDS40 0x109 // 265

\#definire LA \_ VERSIONE \_ CI WIN70 0x700 // 1792

Una volta noto il valore, il client può formare una query supportata dal server ed eseguire una query reale.

DBPROPSET \_ MSIDXS \_ ROWSETEXT è dichiarato in ntquery.h.

 

 
