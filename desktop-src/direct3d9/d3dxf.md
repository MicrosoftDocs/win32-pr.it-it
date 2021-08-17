---
description: Opzioni di formato di file X, caricamento e salvataggio.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d286ad4cf64133683de026893beb9fa081899e6b170e4b3adb478798eb4b3edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096076"
---
# <a name="d3dxf"></a>D3DXF

Opzioni di formato di file X, caricamento e salvataggio.

## <a name="file-formats"></a>Formati di file

Nella tabella seguente viene specificato il tipo di dati del file:



| \#definisce per formato di file     | Valore | Descrizione                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| D3DXF \_ FILEFORMAT \_ BINARY     | 0     | File binario in formato legacy. Vedere [X File Reference (Legacy) (Informazioni di riferimento sul file X (legacy)](dx9-graphics-reference-x-file.md)). |
| D3DXF \_ FILEFORMAT \_ TEXT       | 1     | File di testo.                                                                                     |
| FILEFORMAT D3DXF \_ \_ COMPRESSO | 2     | File compresso. Con questo flag è necessario specificare anche il formato binario o il formato di testo.   |



 

## <a name="file-load-options"></a>Opzioni di caricamento file

La tabella seguente specifica le opzioni di caricamento dei file con file con estensione x:



| \#Definire                      | Valore | Descrizione                |
|-------------------------------|-------|----------------------------|
| D3DXF \_ FILELOAD \_ FromFile     | 0     | Caricare i dati da un file.     |
| D3DXF \_ FILELOAD \_ FROMWFILE    | 1     | Caricare i dati da un file.     |
| D3DXF \_ FILELOAD \_ FROMRESOURCE | 2     | Caricare i dati da una risorsa. |
| D3DXF \_ FILELOAD \_ FROMMEMORY   | 3     | Caricare i dati dalla memoria.     |



 

## <a name="file-save-options"></a>Opzioni di salvataggio file

La tabella seguente specifica le opzioni di salvataggio e caricamento dei file con i file con estensione x:



| \#Definire                 | Valore | Descrizione                    |
|--------------------------|-------|--------------------------------|
| FILE D3DXFSALVA \_ \_ IN FILE  | 0     | Salvare in un file.                |
| FILE D3DXFSALVA \_ \_ TOWFILE | 1     | Salvare in un file a caratteri wide. |



 

## <a name="constant-information"></a>Informazioni sulle costanti



| Requisito                         | Valore           |
|--------------------------|------------|
| Intestazione                   | d3dx9xof.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti file D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[**D3DXSaveMeshToX**](d3dxsavemeshtox.md)
</dt> </dl>

 

 



