---
title: Sintassi di Stream out
description: Un geometry shader con flusso in uscita viene dichiarato con una particolare sintassi.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ea78d1b2109e343f01800b3a3d5e1bf6efaba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992792"
---
# <a name="stream-out-syntax"></a>Sintassi di Stream out

Un geometry shader con flusso in uscita viene dichiarato con una particolare sintassi. In questo argomento viene descritta la sintassi di. Nel runtime degli effetti questa sintassi verrà convertita in una chiamata a [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).

## <a name="construct-syntax"></a>Sintassi del costrutto


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| Nome                   | Descrizione                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | facoltativo. Stringa ASCI che identifica in modo univoco il nome di una variabile di shader Geometry con flusso in uscita. Questa operazione è facoltativa perché ConstructGSWithSO può essere inserito direttamente in una chiamata SetGeometryShader o BindInterfaces. |
| **ShaderVar**          | Una variabile geometry shader o vertex shader.                                                                                                                                                                               |
| **OutputDecl0**        | Stringa che definisce quali output dello shader nel flusso 0 vengono trasmessi. Per la sintassi, vedere di seguito.                                                                                                                                 |



 

Questa è la sintassi definita in file FX \_ 4 \_ 0. Si noti che negli \_ shader GS 4 \_ 0 e vs \_ x è presente un solo flusso di dati. Lo shader risultante restituirà un flusso all'unità di output del flusso e all'unità di rasterizzazione.


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| Nome                   | Descrizione                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **StreamingShaderVar** | facoltativo. Stringa ASCI che identifica in modo univoco il nome di una variabile di shader Geometry con flusso in uscita. Questa operazione è facoltativa perché ConstructGSWithSO può essere inserito direttamente in una chiamata SetGeometryShader o BindInterfaces. |
| **ShaderVar**          | Una variabile geometry shader o vertex shader.                                                                                                                                                                               |
| **OutputDecl0**        | Stringa che definisce quali output dello shader nel flusso 0 vengono trasmessi. Per la sintassi, vedere di seguito.                                                                                                                                 |
| **OutputDecl1**        | Stringa che definisce quali output dello shader nel flusso 1 vengono trasmessi. Per la sintassi, vedere di seguito.                                                                                                                                 |
| **OutputDecl2**        | Stringa che definisce quali output dello shader nel flusso 2 vengono trasmessi. Per la sintassi, vedere di seguito.                                                                                                                                 |
| **OutputDecl3**        | Stringa che definisce quali output dello shader nel flusso 3 vengono trasmessi. Per la sintassi, vedere di seguito.                                                                                                                                 |
| **RasterizedStream**   | Intero che specifica quale flusso verrà inviato al rasterizzatore.                                                                                                                                                         |



 

Si noti che \_ gli \_ shader GS 5 0 possono definire fino a quattro flussi di dati. Lo shader risultante restituirà un flusso all'unità di output del flusso per ogni dichiarazione di output non **null** e un flusso dell'unità di rasterizzazione.

## <a name="stream-out-declaration-syntax"></a>Sintassi della dichiarazione di flusso out


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| Nome              | Descrizione                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| **Buffer**        | facoltativo. Numero intero, 0 <= buffer < 4, che specifica a quale flusso viene inviato il buffer a cui andrà il valore. |
| **Semantica**      | Stringa, insieme a SemanticIndex, che specifica il valore da restituire.                                 |
| **SemanticIndex** | facoltativo. Indice associato a Semantic.                                                         |
| **Mask**          | facoltativo. Maschera di componenti, che indica i componenti del valore da restituire.                       |



 

Esiste una semantica speciale, denominata "$SKIP" che indica una semantica vuota, lasciando invariata la memoria corrispondente nel buffer di flusso. La semantica $SKIP non può avere un SemanticIndex, ma può avere una maschera.

L'intera dichiarazione out del flusso può essere **null**.

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

 

 




