---
description: Oltre ai valori restituiti COM standard, i metodi usati per lavorare con i file DirectX con estensione x possono restituire i valori seguenti.
ms.assetid: b1d04fab-25cb-431d-942e-74092bc9c5c2
title: Valori restituiti D3DXFERR (D3dx9xof.h)
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
ms.openlocfilehash: b6e106fc7163ed4ff66e74332336cc85b2a95afdc0fa6b712b00f3b32e2af248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096066"
---
# <a name="d3dxferr-return-values"></a>Valori restituiti di D3DXFERR

Oltre ai valori restituiti COM standard, i metodi usati per lavorare con i file DirectX con estensione x possono restituire i valori seguenti.

<dl> <dt>

<span id="D3DXFERR_BADARRAYSIZE"></span><span id="d3dxferr_badarraysize"></span>**D3DXFERR \_ BADARRAYSIZE**
</dt> <dd>

Una matrice supera le dimensioni consentite.

</dd> <dt>

<span id="D3DXFERR_BADCACHEFILE"></span><span id="d3dxferr_badcachefile"></span>**D3DXFERR \_ BADCACHEFILE**
</dt> <dd>

Non è stato possibile leggere un file di cache.

</dd> <dt>

<span id="D3DXFERR_BADDataReference"></span><span id="d3dxferr_baddatareference"></span><span id="D3DXFERR_BADDATAREFERENCE"></span>**D3DXFERR \_ BADDataReference**
</dt> <dd>

Non è stato possibile recuperare i dati dei membri del modello.

</dd> <dt>

<span id="D3DXFERR_BADFILE"></span><span id="d3dxferr_badfile"></span>**D3DXFERR \_ BADFILE**
</dt> <dd>

Operazione di lettura o scrittura di file non riuscita.

</dd> <dt>

<span id="D3DXFERR_BADFILEFLOATSIZE"></span><span id="d3dxferr_badfilefloatsize"></span>**D3DXFERR \_ BADFILEFLOATSIZE**
</dt> <dd>

Le dimensioni del file non sono previste.

</dd> <dt>

<span id="D3DXFERR_BADFILETYPE"></span><span id="d3dxferr_badfiletype"></span>**D3DXFERR \_ BADFILETYPE**
</dt> <dd>

Il formato del file non è valido.

</dd> <dt>

<span id="D3DXFERR_BADFILEVERSION"></span><span id="d3dxferr_badfileversion"></span>**D3DXFERR \_ BADFILEVERSION**
</dt> <dd>

La versione del formato del file non è valida.

</dd> <dt>

<span id="D3DXFERR_BADOBJECT"></span><span id="d3dxferr_badobject"></span>**D3DXFERR \_ BADOBJECT**
</dt> <dd>

Non è stato possibile leggere o scrivere dati in un oggetto.

</dd> <dt>

<span id="D3DXFERR_BADRESOURCE"></span><span id="d3dxferr_badresource"></span>**D3DXFERR \_ BADRESOURCE**
</dt> <dd>

Un'operazione su una risorsa non è riuscita.

</dd> <dt>

<span id="D3DXFERR_BADTYPE"></span><span id="d3dxferr_badtype"></span>**D3DXFERR \_ BADTYPE**
</dt> <dd>

Il file non corrisponde a tipi di modello noti.

</dd> <dt>

<span id="D3DXFERR_BADVALUE"></span><span id="d3dxferr_badvalue"></span>**D3DXFERR \_ BADVALUE**
</dt> <dd>

Una variabile non rientra nell'intervallo previsto. in genere restituito quando un puntatore a un oggetto non è valido.

</dd> <dt>

<span id="D3DXFERR_FILENOTFOUND"></span><span id="d3dxferr_filenotfound"></span>**D3DXFERR \_ FILENOTFOUND**
</dt> <dd>

Impossibile trovare un handle valido per il file specificato.

</dd> <dt>

<span id="D3DXFERR_NOMOREDATA"></span><span id="d3dxferr_nomoredata"></span>**D3DXFERR \_ NOMOREDATA**
</dt> <dd>

Offset del puntatore esteso oltre la fine del buffer.

</dd> <dt>

<span id="D3DXFERR_NOMOREOBJECTS"></span><span id="d3dxferr_nomoreobjects"></span>**D3DXFERR \_ NOMOREOBJECTS**
</dt> <dd>

Non sono disponibili altri oggetti figlio.

</dd> <dt>

<span id="D3DXFERR_NOTDONEYET"></span><span id="d3dxferr_notdoneyet"></span>**D3DXFERR \_ NOTDONEYET**
</dt> <dd>

Il tipo di dati non corrisponde ai tipi consentiti.

</dd> <dt>

<span id="D3DXFERR_NOTFOUND"></span><span id="d3dxferr_notfound"></span>**D3DXFERR \_ NOTFOUND**
</dt> <dd>

Impossibile trovare l'oggetto dai parametri specificati.

</dd> <dt>

<span id="D3DXFERR_PARSEERROR"></span><span id="d3dxferr_parseerror"></span>**D3DXFERR \_ PARSEERROR**
</dt> <dd>

Impossibile analizzare il flusso di dati.

</dd> <dt>

<span id="D3DXFERR_RESOURCENOTFOUND"></span><span id="d3dxferr_resourcenotfound"></span>**RISORSA D3DXFERRNOTFOUND \_**
</dt> <dd>

Impossibile trovare un handle valido per la risorsa specificata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il codice di funzionalità di errore del file \_ X FACD3DXF viene usato per generare i codici di errore. Esempio:


```
#define _FACD3DXF           0x876
#define D3DXFERR_BADOBJECT  MAKE_HRESULT( 1, _FACD3DXF, 900 )
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9xof.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti file D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> </dl>

 

 




