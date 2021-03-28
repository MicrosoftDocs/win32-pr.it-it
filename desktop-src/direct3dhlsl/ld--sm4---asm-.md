---
title: LD (SM4-ASM)
description: Recupera i dati dal buffer o dalla trama specificati senza filtrare, ad esempio il campionamento dei punti, usando l'indirizzo integer fornito. I dati di origine possono provenire da qualsiasi tipo di risorsa, diverso da TextureCube.
ms.assetid: DEE9A55F-EDFE-478E-8169-5BF9C43E98AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaacc3d76d49cc2b3043d39036f0ff652d7b8794
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335540"
---
# <a name="ld-sm4---asm"></a>LD (SM4-ASM)

Recupera i dati dal buffer o dalla trama specificati senza filtrare, ad esempio il campionamento dei punti, usando l'indirizzo integer fornito. I dati di origine possono provenire da qualsiasi tipo di risorsa, diverso da TextureCube.



| LD \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle\] |
|----------------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[nell' \] indirizzo del risultato dell'operazione.<br/>                                                               |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[nelle \] coordinate di trama necessarie per eseguire l'esempio.<br/>                                                     |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] un registro di trama (t \# ) che deve essere stato dichiarato che identifica la trama o il buffer da cui recuperare.<br/> |



 

## <a name="remarks"></a>Commenti

Questa istruzione è un'alternativa semplificata all'istruzione di [esempio](sample--sm4---asm-.md) . A differenza di **esempio**, **LD** è anche in grado di recuperare i dati dai buffer. **LD** è anche in grado di recuperare da risorse di più campioni (solo pixel shader).

*srcAddress* fornisce il set di coordinate di trama necessarie per eseguire l'esempio sotto forma di interi senza segno. Se *srcAddress* non è compreso nell'intervallo \[ 0... ( \# Texels nella dimensione 1) \] , viene richiamato il comportamento out-of-Bounds, dove **LD** restituisce 0 in tutti i componenti non mancanti del formato di *srcResource* e il valore predefinito per i componenti mancanti. Un'applicazione che desidera un controllo più flessibile sul comportamento degli indirizzi non compresi nell'intervallo deve invece utilizzare l'istruzione di **esempio** , in quanto rispetta il comportamento di ritorno a capo/mirroring/morsetto/bordo definito come stato del campionatore.

*srcAddress. a* (POS-swizzle) fornisce sempre un livello Unsigned Integer mipmap. Se il valore non è compreso nell'intervallo \[ 0... ( Num mipLevels in Resource-1) \] , viene richiamato il comportamento out-of-Bounds. Se la risorsa è un buffer, che non può avere mipmap, *srcAddress. a* viene ignorato

*srcAddress. GB* (POS-swizzle) viene ignorato per i buffer e texture1D (non matrice). *srcAddress. b* (POS-swizzle) viene ignorato per le matrici Texture1D e texture2Ds.

Per le matrici texture1D, *srcAddress. g* (POS-swizzle) fornisce l'indice della matrice come Unsigned Integer. Se il valore non è compreso nell'intervallo degli indici di matrice disponibili \[ 0... ( dimensione della matrice-1) \] , viene richiamato il comportamento fuori limite.

Per le matrici texture2D, *srcAddress. b* (POS-swizzle) fornisce l'indice della matrice, in caso contrario con la stessa semantica di texture1D.

Il recupero da *t \#* a cui non è associato alcun elemento restituisce 0 per tutti i componenti.

### <a name="address-offset"></a>Offset indirizzo

Il \[ \_ suffisso aoffimmi (u, v, w) facoltativo \] (offset indirizzo per intero immediato) indica che le coordinate di trama per il **LD** devono essere sottoposte a offset in base a un set di valori costanti integer dello spazio Texel immediatamente specificato. I valori letterali sono un set di numeri di complemento a 4 bit, con intervallo di valori integer \[ -8, 7 \] . Questo modificatore è definito solo per texture1D/2D/3D, incluse le matrici e non per i buffer.

Gli offset vengono aggiunti alle coordinate di trama, nello spazio Texel, rispetto alla miplevel a cui si accede tramite **LD**.

Gli offset degli indirizzi non vengono applicati lungo l'asse delle matrici di matrici texture1D/2D.

I componenti *\_ aoffimmi v, w* vengono ignorati per texture1Ds.

Il componente *\_ aoffimmi w* viene ignorato per texture2Ds.

Poiché le coordinate di trama per **LD** sono interi senza segno, se l'offset fa sì che l'indirizzo vada al di sotto di zero, verrà eseguito il wrapping a un indirizzo di grandi dimensioni e il risultato sarà un accesso fuori limite.

### <a name="return-type-control"></a>Controllo tipo restituito

Il formato dati restituito da **LD** al registro di destinazione viene determinato in modo analogo a quanto descritto per l'istruzione di **esempio** . si basa sul formato associato al parametro *srcResource* (*t \#*).

Come per l'istruzione di **esempio** , i valori restituiti per **LD** sono 4 vettori con impostazioni predefinite specifiche del formato per i componenti non presenti nel formato. Il swizzle in *srcResource* determina come swizzle il risultato a 4 componenti restituito dal caricamento della trama, dopo il quale. mask su *dest* determina quali componenti in *dest* vengono aggiornati.

Quando un valore float a 32 bit viene letto da *LD* in un registro a 32 bit, i bit non vengono modificati; ovvero i valori denormali rimangono denormalizzati. Questo è diverso dall'istruzione di **esempio** .

### <a name="miscellaneous-details"></a>Dettagli vari

Poiché non esiste alcun filtro associato all'istruzione **LD** , concetti come la distorsione di LOD non si applicano a **LD**. Di conseguenza non è presente *alcun \# parametro del* campionatore.

### <a name="restrictions"></a>Restrizioni

-   *srcResource* deve essere un \# Registro t e non un TextureCube. *srcResource* non può essere un ConstantBuffer né associato a \# registri t.
-   L'indirizzamento relativo in *srcResource* non è consentito.
-   *srcAddress* deve essere un registro temp (r \# /x \# ), Constant (CB \# ) o input (v \# ).
-   il valore di *dest* deve essere un registro temp (r \# /x \# ) o output (o \* \# ).

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





