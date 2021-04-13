---
description: Una striscia triangolare è una serie di triangoli connessi.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Strisce triangolari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2766529a37b994e5fe30815ca6300476f06c7d4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568453"
---
# <a name="triangle-strips"></a>Strisce triangolari

Una striscia triangolare è una serie di triangoli connessi. Poiché i triangoli sono connessi, non è necessario che l'applicazione specifichi ripetutamente tutti e tre i vertici per ogni triangolo. Ad esempio, per definire la striscia di triangolo seguente sono necessari solo sette vertici.

![illustrazione di una striscia di triangolo con sette vertici](images/tristrip.png)

Il sistema usa i vertici V1, V2 e V3 per creare il primo triangolo; V2, V4 e V3 per creare il secondo triangolo; V3, V4 e V5 per creare il terzo; V4, V6 e V5 per creare il quarto; E così via. Si noti che i vertici del secondo e del quarto triangoli non sono ordinati. Questa operazione è necessaria per garantire che tutti i triangoli siano disegnati in un orientamento orario.

La maggior parte degli oggetti nelle scene 3D è costituita da strisce di triangolo. Questo è dovuto al fatto che le strisce triangolari possono essere utilizzate per specificare oggetti complessi in modo da utilizzare in modo efficiente la memoria e i tempi di elaborazione.

Nella figura seguente viene illustrata una striscia di triangolo sottoposta a rendering.

![illustrazione di una striscia di triangolo sottoposta a rendering](images/tstrip2.png)

Il codice seguente illustra come creare vertici per questa striscia di triangolo.


```
struct CUSTOMVERTEX
{
float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



L'esempio di codice seguente illustra come eseguire il rendering di questa striscia di triangolo in Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



Usare una striscia di triangolo per eseguire il rendering di triangoli non connessi tra loro. A tale scopo, specificare un triangolo degenerato (ovvero un triangolo la cui area è zero) nell'elenco dei triangoli. Viene creata una linea tra i due triangoli che non verrà sottoposta a rendering. Per eseguire il rendering solo dei primi e degli ultimi triangoli dell'esempio precedente, modificare il buffer del vertice come illustrato di seguito:


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitives](primitives.md)
</dt> </dl>

 

 
