---
description: Metadati del supporto
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Metadati del supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb17f286673663976e17b4178239507765c2101
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320703"
---
# <a name="media-metadata"></a>Metadati del supporto

I file multimediali contengono proprietà che descrivono il contenuto del file. In Microsoft Media Foundation, queste proprietà possono essere categorizzate come indicato di seguito:

-   **Gli attributi di tipo supporto** specificano i parametri di codifica, ad esempio l'algoritmo di codifica (sottotipo di supporto), le dimensioni del fotogramma video, la frequenza dei fotogrammi video, la velocità in bit audio e la frequenza di campionamento audio. Per ulteriori informazioni sugli attributi di tipo media, vedere [tipi di supporto](media-types.md).
-   I **metadati** contengono informazioni descrittive per il contenuto multimediale, ad esempio titolo, artista, compositore e genere. I metadati possono anche descrivere i parametri di codifica. Può essere più veloce accedere a queste informazioni tramite metadati rispetto agli attributi di tipo supporto.
-   Le **Proprietà DRM** contengono informazioni sulle restrizioni di utilizzo. Attualmente Media Foundation non supporta le proprietà DRM tramite i metadati, ad eccezione della proprietà **\_ \_ protetta da pkey DRM** .

Esistono due modi per leggere i metadati in Media Foundation:

-   Interfaccia [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (metadati Media Foundation versione 1).
-   L'interfaccia di Windows Shell [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) (metadati della Shell).

I metadati della shell sono relativi non solo ai file multimediali ma a una gamma molto più ampia di file nel sistema.

Nella tabella seguente vengono confrontate le caratteristiche e le limitazioni di ogni API dei metadati.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Metadati di Media Foundation V1</th>
<th>Metadati della shell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Richiede Windows Vista o versione successiva.</td>
<td>Richiede Windows 7.
<blockquote>
[!Note]<br />
I metadati della shell in generale non richiedono Windows 7, ma Media Foundation non supportava i metadati della shell prima di Windows 7.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Le proprietà non sono compatibili con il sistema di proprietà della shell.</td>
<td>Le proprietà sono compatibili con il sistema di proprietà della shell.</td>
</tr>
<tr class="odd">
<td>Le proprietà possono essere valide per l'intero file o a livello di flusso.</td>
<td>Sono supportate solo le proprietà a livello di file. Le proprietà a livello di flusso non sono supportate.</td>
</tr>
<tr class="even">
<td>Le proprietà possono avere valori in più lingue.</td>
<td>I valori in più lingue non sono supportati.</td>
</tr>
<tr class="odd">
<td>Le chiavi delle proprietà sono stringhe a caratteri wide.</td>
<td>Le chiavi delle proprietà sono valori <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PropertyKey</strong></a> .</td>
</tr>
<tr class="even">
<td>I valori delle proprietà sono valori <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</td>
<td>I valori delle proprietà sono valori <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</td>
</tr>
</tbody>
</table>



 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                     | Descrizione                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Provider di metadati della shell](shell-metadata-providers.md)<br/>                       | A partire da Windows 7, Media Foundation espone i metadati tramite l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .<br/> |
| [Proprietà dei metadati dei file multimediali](metadata-properties-for-media-files.md)<br/> | Questo argomento elenca le proprietà dei metadati più comuni per i file multimediali.<br/>                                                           |
| [Provider di metadati in Windows Vista](metadata-providers-in-windows-vista.md)<br/> | In Windows Vista Media Foundation espone i metadati tramite l'interfaccia [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .<br/>                   |



 

Se si implementa un'origine multimediale personalizzata e si vuole esporre i metadati della shell, vedere [provider di metadati personalizzati per i file multimediali](custom-metadata-providers-for-media-files.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 
