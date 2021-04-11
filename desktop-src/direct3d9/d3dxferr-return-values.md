---
description: I metodi usati per lavorare con i file DirectX. x possono restituire i valori seguenti oltre ai valori restituiti standard COM.
ms.assetid: b1d04fab-25cb-431d-942e-74092bc9c5c2
title: Valori restituiti D3DXFERR (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFERR
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: cab1cc5e70b6204c832fd9fe5b0fecac4276f578
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132343"
---
# <a name="d3dxferr-return-values"></a>Valori restituiti D3DXFERR

I metodi usati per lavorare con i file DirectX. x possono restituire i valori seguenti oltre ai valori restituiti standard COM.

<dl> <dt>

<span id="D3DXFERR_BADARRAYSIZE"></span><span id="d3dxferr_badarraysize"></span>**\_BADARRAYSIZE D3DXFERR**
</dt> <dd>

Una matrice supera la dimensione consentita.

</dd> <dt>

<span id="D3DXFERR_BADCACHEFILE"></span><span id="d3dxferr_badcachefile"></span>**\_BADCACHEFILE D3DXFERR**
</dt> <dd>

Impossibile leggere un file di cache.

</dd> <dt>

<span id="D3DXFERR_BADDataReference"></span><span id="d3dxferr_baddatareference"></span><span id="D3DXFERR_BADDATAREFERENCE"></span>**\_BADDATAREFERENCE D3DXFERR**
</dt> <dd>

Impossibile recuperare i dati dei membri del modello.

</dd> <dt>

<span id="D3DXFERR_BADFILE"></span><span id="d3dxferr_badfile"></span>**\_BadFile D3DXFERR**
</dt> <dd>

Operazione di lettura o scrittura del file non riuscita.

</dd> <dt>

<span id="D3DXFERR_BADFILEFLOATSIZE"></span><span id="d3dxferr_badfilefloatsize"></span>**\_BADFILEFLOATSIZE D3DXFERR**
</dt> <dd>

Il file non è di dimensioni previste.

</dd> <dt>

<span id="D3DXFERR_BADFILETYPE"></span><span id="d3dxferr_badfiletype"></span>**\_BADFILETYPE D3DXFERR**
</dt> <dd>

Il formato del file non è valido.

</dd> <dt>

<span id="D3DXFERR_BADFILEVERSION"></span><span id="d3dxferr_badfileversion"></span>**\_BADFILEVERSION D3DXFERR**
</dt> <dd>

La versione del formato del file non è valida.

</dd> <dt>

<span id="D3DXFERR_BADOBJECT"></span><span id="d3dxferr_badobject"></span>**\_BADOBJECT D3DXFERR**
</dt> <dd>

Impossibile leggere o scrivere dati in un oggetto.

</dd> <dt>

<span id="D3DXFERR_BADRESOURCE"></span><span id="d3dxferr_badresource"></span>**\_BADRESOURCE D3DXFERR**
</dt> <dd>

Un'operazione su una risorsa non è riuscita.

</dd> <dt>

<span id="D3DXFERR_BADTYPE"></span><span id="d3dxferr_badtype"></span>**\_BADTYPE D3DXFERR**
</dt> <dd>

Il file non corrisponde ai tipi di modello noti.

</dd> <dt>

<span id="D3DXFERR_BADVALUE"></span><span id="d3dxferr_badvalue"></span>**\_BADVALUE D3DXFERR**
</dt> <dd>

Una variabile non è compresa nell'intervallo previsto; restituito in genere quando un puntatore a un oggetto non è valido.

</dd> <dt>

<span id="D3DXFERR_FILENOTFOUND"></span><span id="d3dxferr_filenotfound"></span>**\_FileNotFound D3DXFERR**
</dt> <dd>

Impossibile trovare un handle valido per il file specificato.

</dd> <dt>

<span id="D3DXFERR_NOMOREDATA"></span><span id="d3dxferr_nomoredata"></span>**\_NOMOREDATA D3DXFERR**
</dt> <dd>

Offset del puntatore esteso oltre la fine del buffer.

</dd> <dt>

<span id="D3DXFERR_NOMOREOBJECTS"></span><span id="d3dxferr_nomoreobjects"></span>**\_NOMOREOBJECTS D3DXFERR**
</dt> <dd>

Non sono disponibili altri oggetti figlio.

</dd> <dt>

<span id="D3DXFERR_NOTDONEYET"></span><span id="d3dxferr_notdoneyet"></span>**\_NOTDONEYET D3DXFERR**
</dt> <dd>

Il tipo di dati non corrisponde ai tipi consentiti.

</dd> <dt>

<span id="D3DXFERR_NOTFOUND"></span><span id="d3dxferr_notfound"></span>**\_NotFound D3DXFERR**
</dt> <dd>

Impossibile trovare l'oggetto dai parametri specificati.

</dd> <dt>

<span id="D3DXFERR_PARSEERROR"></span><span id="d3dxferr_parseerror"></span>**D3DXFERR ( \_ PARSEERROR)**
</dt> <dd>

Non è stato possibile analizzare il flusso di dati.

</dd> <dt>

<span id="D3DXFERR_RESOURCENOTFOUND"></span><span id="d3dxferr_resourcenotfound"></span>**\_RESOURCENOTFOUND D3DXFERR**
</dt> <dd>

Impossibile trovare un handle valido per la risorsa specificata.

</dd> </dl>

## <a name="remarks"></a>Commenti

\_Per generare i codici di errore viene usato il codice della funzionalità di errore file con estensione x FACD3DXF. Ad esempio:


```
#define _FACD3DXF           0x876
#define D3DXFERR_BADOBJECT  MAKE_HRESULT( 1, _FACD3DXF, 900 )
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti file D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> </dl>

 

 




