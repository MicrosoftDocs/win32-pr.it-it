---
description: I metodi usati per lavorare con i file DirectX. x possono restituire i valori seguenti oltre ai valori restituiti standard COM. Deprecato.
ms.assetid: a91168bc-966a-47b5-ba83-fc480593228d
title: Valori restituiti (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Return
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 7d465b9759d958cba06bf0b950bc67772fbb84a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762131"
---
# <a name="return-values-dxfileh"></a>Valori restituiti (DXFile. h)

I metodi usati per lavorare con i file DirectX. x possono restituire i valori seguenti oltre ai valori restituiti standard COM. Deprecato.

<dl> <dt>

<span id="DXFILE_OK"></span><span id="dxfile_ok"></span>**DXFILE \_ OK**
</dt> <dd>

Comando completato correttamente.

</dd> <dt>

<span id="DXFILEERR_BADALLOC"></span><span id="dxfileerr_badalloc"></span>**\_BADALLOC DXFILEERR**
</dt> <dd>

L'allocazione di memoria ha avuto esito negativo.

</dd> <dt>

<span id="DXFILEERR_BADARRAYSIZE"></span><span id="dxfileerr_badarraysize"></span>**\_BADARRAYSIZE DXFILEERR**
</dt> <dd>

La dimensione della matrice non è valida.

</dd> <dt>

<span id="DXFILEERR_BADCACHEFILE"></span><span id="dxfileerr_badcachefile"></span>**\_BADCACHEFILE DXFILEERR**
</dt> <dd>

Il file di cache contenente la data del file con estensione x non è valido. Un file di cache contiene i dati recuperati dalla rete, memorizzati nella cache sul disco rigido e recuperati nelle richieste successive.

</dd> <dt>

<span id="DXFILEERR_BADDataReference"></span><span id="dxfileerr_baddatareference"></span><span id="DXFILEERR_BADDATAREFERENCE"></span>**\_BADDATAREFERENCE DXFILEERR**
</dt> <dd>

Riferimento ai dati non valido.

</dd> <dt>

<span id="DXFILEERR_BADFILE"></span><span id="dxfileerr_badfile"></span>**\_BadFile DXFILEERR**
</dt> <dd>

Il file non è valido.

</dd> <dt>

<span id="DXFILEERR_BADFILECOMPRESSIONTYPE"></span><span id="dxfileerr_badfilecompressiontype"></span>**\_BADFILECOMPRESSIONTYPE DXFILEERR**
</dt> <dd>

Il tipo di compressione del file non è valido.

</dd> <dt>

<span id="DXFILEERR_BADFILEFLOATSIZE"></span><span id="dxfileerr_badfilefloatsize"></span>**\_BADFILEFLOATSIZE DXFILEERR**
</dt> <dd>

Le dimensioni a virgola mobile non sono valide.

</dd> <dt>

<span id="DXFILEERR_BADFILETYPE"></span><span id="dxfileerr_badfiletype"></span>**\_BADFILETYPE DXFILEERR**
</dt> <dd>

Il file non è un file DirectX. x.

</dd> <dt>

<span id="DXFILEERR_BADFILEVERSION"></span><span id="dxfileerr_badfileversion"></span>**\_BADFILEVERSION DXFILEERR**
</dt> <dd>

La versione del file non è valida.

</dd> <dt>

<span id="DXFILEERR_BADINTRINSICS"></span><span id="dxfileerr_badintrinsics"></span>**\_BADINTRINSICS DXFILEERR**
</dt> <dd>

Gli intrinseci non sono validi.

</dd> <dt>

<span id="DXFILEERR_BADOBJECT"></span><span id="dxfileerr_badobject"></span>**\_BADOBJECT DXFILEERR**
</dt> <dd>

Oggetto non valido.

</dd> <dt>

<span id="DXFILEERR_BADRESOURCE"></span><span id="dxfileerr_badresource"></span>**\_BADRESOURCE DXFILEERR**
</dt> <dd>

La risorsa non è valida.

</dd> <dt>

<span id="DXFILEERR_BADSTREAMHANDLE"></span><span id="dxfileerr_badstreamhandle"></span>**\_BADSTREAMHANDLE DXFILEERR**
</dt> <dd>

Handle del flusso non valido.

</dd> <dt>

<span id="DXFILEERR_BADTYPE"></span><span id="dxfileerr_badtype"></span>**\_BADTYPE DXFILEERR**
</dt> <dd>

Il tipo di oggetto non è valido.

</dd> <dt>

<span id="DXFILEERR_BADVALUE"></span><span id="dxfileerr_badvalue"></span>**\_BADVALUE DXFILEERR**
</dt> <dd>

Il parametro non è valido.

</dd> <dt>

<span id="DXFILEERR_FILENOTFOUND"></span><span id="dxfileerr_filenotfound"></span>**\_FileNotFound DXFILEERR**
</dt> <dd>

Il file non è stato trovato.

</dd> <dt>

<span id="DXFILEERR_INTERNALERROR"></span><span id="dxfileerr_internalerror"></span>**\_INTERNALERROR DXFILEERR**
</dt> <dd>

Si è verificato un errore interno.

</dd> <dt>

<span id="DXFILEERR_NOINTERNET"></span><span id="dxfileerr_nointernet"></span>**DXFILEERR \_ NOinternet**
</dt> <dd>

Connessione Internet non trovata.

</dd> <dt>

<span id="DXFILEERR_NOMOREDATA"></span><span id="dxfileerr_nomoredata"></span>**\_NOMOREDATA DXFILEERR**
</dt> <dd>

Non sono disponibili altri dati.

</dd> <dt>

<span id="DXFILEERR_NOMOREOBJECTS"></span><span id="dxfileerr_nomoreobjects"></span>**\_NOMOREOBJECTS DXFILEERR**
</dt> <dd>

Tutti gli oggetti sono stati enumerati.

</dd> <dt>

<span id="DXFILEERR_NOMORESTREAMHANDLES"></span><span id="dxfileerr_nomorestreamhandles"></span>**\_NOMORESTREAMHANDLES DXFILEERR**
</dt> <dd>

Non sono disponibili handle di flusso.

</dd> <dt>

<span id="DXFILEERR_NOTDONEYET"></span><span id="dxfileerr_notdoneyet"></span>**\_NOTDONEYET DXFILEERR**
</dt> <dd>

Operazione non completata.

</dd> <dt>

<span id="DXFILEERR_NOTFOUND"></span><span id="dxfileerr_notfound"></span>**\_NotFound DXFILEERR**
</dt> <dd>

Impossibile trovare l'oggetto.

</dd> <dt>

<span id="DXFILEERR_PARSEERROR"></span><span id="dxfileerr_parseerror"></span>**DXFILEERR ( \_ PARSEERROR)**
</dt> <dd>

Non è stato possibile analizzare il file.

</dd> <dt>

<span id="DXFILEERR_RESOURCENOTFOUND"></span><span id="dxfileerr_resourcenotfound"></span>**\_RESOURCENOTFOUND DXFILEERR**
</dt> <dd>

Impossibile trovare la risorsa.

</dd> <dt>

<span id="DXFILEERR_NOTEMPLATE"></span><span id="dxfileerr_notemplate"></span>**notemplate DXFILEERR \_**
</dt> <dd>

Non sono disponibili modelli.

</dd> <dt>

<span id="DXFILEERR_URLNOTFOUND"></span><span id="dxfileerr_urlnotfound"></span>**\_URLNOTFOUND DXFILEERR**
</dt> <dd>

Impossibile trovare l'URL.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>DXFile. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento file X (legacy)](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 




