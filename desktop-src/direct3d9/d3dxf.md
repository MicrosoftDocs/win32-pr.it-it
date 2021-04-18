---
description: X formato file, caricamento e opzioni di salvataggio.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073887c6cc93754ead01ce379310a9be09edc88f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303690"
---
# <a name="d3dxf"></a>D3DXF

X formato file, caricamento e opzioni di salvataggio.

## <a name="file-formats"></a>Formati di file

Nella tabella seguente viene specificato il tipo di dati del file:



| \#definisce per il formato di file     | Valore | Descrizione                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| \_Binario FILEFORMAT \_ D3DXF     | 0     | File binario in formato legacy. Vedere il [riferimento al file X (legacy)](dx9-graphics-reference-x-file.md). |
| \_Testo FILEformat D3DXF \_       | 1     | File di testo.                                                                                     |
| D3DXF \_ FileFormat \_ compresso | 2     | File compresso. Con questo flag, è necessario specificare anche il formato binario o il formato di testo.   |



 

## <a name="file-load-options"></a>Opzioni di caricamento file

Nella tabella seguente vengono specificate le opzioni di caricamento file con i file con estensione x:



| \#definire                      | Valore | Descrizione                |
|-------------------------------|-------|----------------------------|
| D3DXF \_ fileload \_ FromFile     | 0     | Caricare i dati da un file.     |
| D3DXF \_ fileload \_ FROMWFILE    | 1     | Caricare i dati da un file.     |
| D3DXF \_ fileload \_ FROMRESOURCE | 2     | Caricare i dati da una risorsa. |
| D3DXF \_ fileload \_ FROMMEMORY   | 3     | Caricare i dati dalla memoria.     |



 

## <a name="file-save-options"></a>Opzioni di salvataggio file

La tabella seguente specifica le opzioni di salvataggio e caricamento dei file con i file con estensione x:



| \#definire                 | Valore | Descrizione                    |
|--------------------------|-------|--------------------------------|
| \_File D3DXF FILEsave \_  | 0     | Salva in un file.                |
| D3DXF \_ FileSave \_ TOWFILE | 1     | Salva in un file a caratteri wide. |



 

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3dx9xof. h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti file D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[**D3DXSaveMeshToX**](d3dxsavemeshtox.md)
</dt> </dl>

 

 



