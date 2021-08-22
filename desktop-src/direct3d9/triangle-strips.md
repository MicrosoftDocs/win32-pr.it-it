---
description: Una striscia triangolare è una serie di triangoli connessi.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Strisce triangolare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf229883fa156afc93ca2889a0a97f4f2c3eabbb344fb7551476c98f33905f8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044109"
---
# <a name="triangle-strips"></a>Strisce triangolare

Una striscia triangolare è una serie di triangoli connessi. Poiché i triangoli sono connessi, l'applicazione non deve specificare ripetutamente tutti e tre i vertici per ogni triangolo. Ad esempio, sono necessari solo sette vertici per definire la striscia triangolare seguente.

![illustrazione di una striscia triangolare con sette vertici](images/tristrip.png)

Il sistema usa i vertici v1, v2 e v3 per disegnare il primo triangolo. v2, v4 e v3 per disegnare il secondo triangolo; v3, v4 e v5 per disegnare il terzo; v4, v6 e v5 per disegnare il quarto; E così via. Si noti che i vertici del secondo e del quarto triangolo non sono in ordine. Questa operazione è necessaria per assicurarsi che tutti i triangoli siano disegnati con orientamento in senso orario.

La maggior parte degli oggetti nelle scene 3D è costituita da strisce di triangoli. Ciò è dovuto al fatto che le strisce di triangolo possono essere usate per specificare oggetti complessi in modo da usare in modo efficiente la memoria e il tempo di elaborazione.

La figura seguente illustra una striscia triangolare sottoposta a rendering.

![illustrazione di una striscia triangolare sottoposta a rendering](images/tstrip2.png)

Il codice seguente illustra come creare vertici per questa striscia triangolare.


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



L'esempio di codice seguente illustra come eseguire il rendering di questa striscia triangolare in Direct3D 9 [**usando IDirect3DDevice9::D rawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



Usare una striscia triangolare per eseguire il rendering di triangoli non connessi tra loro. A tale scopo, specificare un triangolo degenere (ovvero un triangolo la cui area è zero) nell'elenco dei triangoli. Verrà creata una linea tra i due triangoli di cui non verrà eseguito il rendering. Per eseguire il rendering solo del primo e dell'ultimo triangolo dell'esempio precedente, modificare il buffer dei vertici come illustrato di seguito:


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

 

 
