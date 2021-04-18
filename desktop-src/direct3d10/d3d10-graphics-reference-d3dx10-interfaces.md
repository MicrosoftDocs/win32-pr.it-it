---
description: Questa sezione contiene informazioni di riferimento per le interfacce COM (Component Object Model) fornite dalla libreria di utilità D3DX. Con la libreria di utilità D3DX vengono utilizzate le interfacce seguenti.
ms.assetid: c57d9c39-3f30-4205-9b0a-665fe53f2b14
title: Interfacce D3DX (grafica Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e0fc152468efec4e33fd6a3ab467d211cfbef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305118"
---
# <a name="d3dx-interfaces-direct3d-10-graphics"></a>Interfacce D3DX (grafica Direct3D 10)

Questa sezione contiene informazioni di riferimento per le interfacce COM (Component Object Model) fornite dalla libreria di utilità D3DX. Con la libreria di utilità D3DX vengono utilizzate le interfacce seguenti.



| Interfacce                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaccia ID3DX10DataLoader**](id3dx10dataloader.md)       | Oggetto caricamento dati utilizzato dall' [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per il caricamento asincrono dei dati.<br/>                                                                                                                                                                                                                                                                                                   |
| [**Interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md) | Oggetto di elaborazione dati utilizzato dall' [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per l'elaborazione asincrona dei dati caricati.<br/>                                                                                                                                                                                                                                                                                      |
| [**Interfaccia ID3DX10Font**](id3dx10font.md)                   | L'interfaccia ID3DX10Font incapsula le trame e le risorse necessarie per eseguire il rendering di un tipo di carattere specifico in un dispositivo specifico.<br/>                                                                                                                                                                                                                                                                                                |
| [**Interfaccia ID3DX10Mesh**](id3dx10mesh.md)                   | Per modificare gli oggetti mesh, le applicazioni utilizzano i metodi dell'interfaccia ID3DX10Mesh.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**Interfaccia ID3DX10MeshBuffer**](id3dx10meshbuffer.md)       |                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**Interfaccia ID3DX10SkinInfo**](id3dx10skininfo.md)           | ID3DX10SkinInfo consente di ottimizzare, elaborare e impostare manualmente la relazione tra le ossa e i vertici nelle mesh (vedere [animazione scheletrica su Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)). È particolarmente utile per la creazione di file con estensione x esportati da app DCC (ad esempio 3DS Max e Maya) più intuitivi e per il miglioramento della velocità di rendering delle mesh con skin in modalità di rendering software.<br/> |
| [**Interfaccia ID3DX10Sprite**](id3dx10sprite.md)               | L'interfaccia ID3DX10Sprite fornisce un set di metodi che semplificano il processo di creazione di sprite con Microsoft Direct3D.<br/>                                                                                                                                                                                                                                                                                            |
| [**Interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)       | Utilizzato per eseguire le attività in modo asincrono. Questo oggetto occupa una quantità considerevole di risorse, quindi in genere è necessario crearne solo una per ogni applicazione.<br/>                                                                                                                                                                                                                                                                  |
| [**Interfaccia ID3DXMatrixStack**](d3d10-id3dxmatrixstack.md)   | Le applicazioni utilizzano i metodi dell'interfaccia ID3DXMATRIXStack per modificare uno stack di matrici.<br/>                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento a D3DX](d3d10-graphics-reference-d3dx10.md)
</dt> </dl>

 

 




