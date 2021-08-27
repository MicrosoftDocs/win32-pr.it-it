---
title: Sintassi di flusso in uscita
description: Un geometry shader con flusso out viene dichiarato con una particolare sintassi.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43980d79d9c338a965d7ab2f2ceb008411d9713dec935d953dd5a1854c40465b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096391"
---
# <a name="stream-out-syntax"></a>Sintassi di flusso in uscita

Un geometry shader con flusso out viene dichiarato con una particolare sintassi. In questo argomento viene descritta la sintassi di . Nel runtime dell'effetto questa sintassi verrà convertita in una chiamata a [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).

## <a name="construct-syntax"></a>Sintassi dei costrutti


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| Nome                   | Descrizione                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | facoltativo. Stringa ASCI che identifica in modo univoco il nome di una variabile geometry shader con stream out. Questo è facoltativo perché ConstructGSWithSO può essere inserito direttamente in una chiamata a SetGeometryShader o BindInterfaces. |
| **ShaderVar**          | Variabile geometry shader o vertex shader.                                                                                                                                                                               |
| **OutputDecl0**        | Stringa che definisce quali output dello shader nel flusso 0 vengono trasmessi. Per la sintassi, vedere di seguito.                                                                                                                                 |



 

Si tratta della sintassi definita nei file fx \_ 4 \_ 0. Si noti che negli shader gs \_ 4 \_ 0 e \_ vs x è presente un solo flusso di dati. Lo shader risultante restituisce un flusso sia all'unità di flusso in uscita che all'unità di rasterizzazione.


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| Nome                   | Descrizione                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | facoltativo. Stringa ASCI che identifica in modo univoco il nome di una variabile geometry shader con stream out. Questo è facoltativo perché ConstructGSWithSO può essere inserito direttamente in una chiamata a SetGeometryShader o BindInterfaces. |
| **ShaderVar**          | Variabile geometry shader o vertex shader.                                                                                                                                                                               |
| **OutputDecl0**        | Stringa che definisce quali output dello shader nel flusso 0 vengono trasmessi. Per la sintassi, vedere di seguito.                                                                                                                                 |
| **OutputDecl1**        | Stringa che definisce quali output dello shader nel flusso 1 vengono trasmessi. Per la sintassi, vedere di seguito.                                                                                                                                 |
| **OutputDecl2**        | Stringa che definisce quali output dello shader nel flusso 2 vengono trasmessi. Per la sintassi, vedere di seguito.                                                                                                                                 |
| **OutputDecl3**        | Stringa che definisce quali output dello shader nel flusso 3 vengono trasmessi in streaming. Per la sintassi, vedere di seguito.                                                                                                                                 |
| **RasterizedStream**   | Intero che specifica il flusso che verrà inviato al rasterizzatore.                                                                                                                                                         |



 

Si noti che gli shader gs \_ \_ 5 0 possono definire fino a quattro flussi di dati. Lo shader risultante restituisce un flusso all'unità di uscita del flusso per ogni dichiarazione di output non **NULL** e un flusso all'unità di rasterizzazione.

## <a name="stream-out-declaration-syntax"></a>Sintassi di dichiarazione di flusso in uscita


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| Nome              | Descrizione                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| **Buffer**        | facoltativo. Intero, 0 <= Buffer < 4, che specifica il buffer di flusso in uscita a cui verrà aggiunto il valore. |
| **Semantica**      | Stringa, insieme a SemanticIndex, che specifica il valore da visualizzare come output.                                 |
| **SemanticIndex** | facoltativo. Indice associato a Semantic.                                                         |
| **Mask**          | facoltativo. Maschera componente, che indica i componenti del valore da determinare.                       |



 

Esiste una semantica speciale, con etichetta "$SKIP" che indica una semantica vuota, lasciando invariata la memoria corrispondente nel buffer di uscita del flusso. La $SKIP semantica non può avere SemanticIndex, ma può avere una maschera.

L'intero flusso di dichiarazione out può essere **NULL.**

## <a name="example"></a>Esempio


```
struct GSOutput
{
int4 Pos : Position;
int4 Color : Color;
int4 Texcoord : Texcoord;
};

[maxvertexcount(1)]
void gsBase (inout PointStream<GSOutput> OutputStream, inout PointStream<GSOutput> OutputStream1)
{
GSOutput output;
output.Pos = int4(1,2,3,4);
output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream.Append(output);

output.Pos = int4(1,2,3,4);
    output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream1.Append(output);
};


GeometryShader pGSComp = CompileShader(gs_5_0, gsBase());
GeometryShader pGSwSO = ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                   "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1);

// The following two passes perform the same operation
technique11 SOPoints
{
    pass 
    {
        SetGeometryShader(ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                     "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1));
    }
    pass 
    {
        SetGeometryShader(pGSwSO);
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




