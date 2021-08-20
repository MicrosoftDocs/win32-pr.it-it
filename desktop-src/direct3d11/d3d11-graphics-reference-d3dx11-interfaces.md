---
title: Interfacce D3DX (grafica Direct3D 11)
description: Questa sezione contiene informazioni di riferimento per le interfacce COM (Component Object Model) fornite dalla libreria di utilità D3DX.
ms.assetid: 0d3be1e6-b558-4586-9440-251a5611d7cd
keywords:
- Interfacce D3DX, Direct3D 11
- interfacce, Direct3D 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd67f82d3198ef25254b3a682c80dc98e0313321
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475738"
---
# <a name="d3dx-interfaces-direct3d-11-graphics"></a>Interfacce D3DX (grafica Direct3D 11)

Questa sezione contiene informazioni di riferimento per le interfacce COM (Component Object Model) fornite dalla libreria di utilità D3DX.

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 


## <a name="in-this-section"></a>Contenuto della sezione




| Argomento | Descrizione | 
|-------|-------------|
| <a href="id3dx11dataloader.md"><strong>ID3DX11DataLoader</strong></a><br /> | <blockquote>[!Note]<br />La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</blockquote><br /> Oggetto di caricamento dati usato <a href="id3dx11threadpump.md"><strong>dall'interfaccia ID3DX11ThreadPump per</strong></a> il caricamento asincrono dei dati.<br /> | 
| <a href="id3dx11dataprocessor.md"><strong>ID3DX11DataProcessor</strong></a><br /> | <blockquote>[!Note]<br />La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</blockquote><br /> Oggetto di elaborazione dati usato <a href="id3dx11threadpump.md"><strong>dall'interfaccia ID3DX11ThreadPump per</strong></a> il caricamento asincrono dei dati.<br /> | 
| <a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump</strong></a><br /> | <blockquote>[!Note]<br />La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</blockquote><br /> Un thread pump esegue le attività in modo asincrono. Viene creato chiamando <a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump.</strong></a> Esistono diverse API che accettano un thread pump facoltativo come parametro, ad esempio <a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a> e <a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a>; Se si passa un'interfaccia pump di thread in queste API, le funzioni verranno eseguite in modo asincrono in un thread separato. In particolare nei computer multiprocessore, una pompa di thread può caricare le risorse ed elaborare i dati senza una notevole riduzione delle prestazioni.<br /> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

 





