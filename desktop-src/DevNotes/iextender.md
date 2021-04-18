---
description: L'interfaccia IExtender fornisce un set di proprietà di base che vengono aggiunte all'interfaccia di un controllo. I programmatori possono usare queste proprietà come se facessero parte del controllo.
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: Interfaccia IExtender
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender
- IExtender.Align
- IExtender.get_Align
- IExtender.put_Align
- IExtender.Enabled
- IExtender.get_Enabled
- IExtender.put_Enabled
- IExtender.Height
- IExtender.get_Height
- IExtender.put_Height
- IExtender.Left
- IExtender.get_Left
- IExtender.put_Left
- IExtender.TabStop
- IExtender.get_TabStop
- IExtender.put_TabStop
- IExtender.Top
- IExtender.get_Top
- IExtender.put_Top
- IExtender.Visible
- IExtender.get_Visible
- IExtender.put_Visible
- IExtender.Width
- IExtender.get_Width
- IExtender.put_Width
- IExtender.Name
- IExtender.get_Name
- IExtender.Parent
- IExtender.get_Parent
- IExtender.Hwnd
- IExtender.get_Hwnd
- IExtender.Container
- IExtender.get_Container
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: fd600de816889e1c644a0e6074d9b8a97e0ec80c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324972"
---
# <a name="iextender-interface"></a>Interfaccia IExtender

L'interfaccia **IExtender** fornisce un set di proprietà di base che vengono aggiunte all'interfaccia di un controllo. I programmatori possono usare queste proprietà come se facessero parte del controllo.

## <a name="members"></a>Membri

L'interfaccia **IExtender** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IExtender** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IExtender** dispone di questi metodi.



| Metodo                         | Descrizione                                    |
|:-------------------------------|:-----------------------------------------------|
| [**Spostare**](iextender-move.md) | Sposta un MDIForm, un form o un controllo.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IExtender** ha queste proprietà.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Proprietà</th>
<th style="text-align: left;">Tipo di accesso</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Allinea<br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Restituisce o imposta un valore che determina se un oggetto viene visualizzato in qualsiasi dimensione in un form o se viene visualizzato in alto, in basso, a sinistra o a destra del form e viene ridimensionato automaticamente per adattarsi alla larghezza del form.<br/> 
<table>
<thead>
<tr class="header">
<th>Costante</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>vbAlignNone 0</td>
<td>(Impostazione predefinita in un form non MDI) None: le dimensioni e la posizione possono essere impostate in fase di progettazione o nel codice. L'impostazione viene ignorata se l'oggetto si trova in un form MDI.</td>
</tr>
<tr class="even">
<td>vbAlignTop 1</td>
<td>(Impostazione predefinita in un form MDI) Top: l'oggetto si trova nella parte superiore del form e la relativa larghezza è uguale all'impostazione della proprietà ScaleWidth del form.</td>
</tr>
<tr class="odd">
<td>vbAlignBottom 2</td>
<td>In basso: l'oggetto si trova nella parte inferiore del form e la relativa larghezza è uguale all'impostazione della proprietà ScaleWidth del form.</td>
</tr>
<tr class="even">
<td>vbAlignLeft 3</td>
<td>Left: l'oggetto si trova a sinistra del form e la relativa larghezza è uguale all'impostazione della proprietà ScaleWidth del form.</td>
</tr>
<tr class="odd">
<td>vbAlignRight 4</td>
<td>Right: l'oggetto si trova a destra del form e la sua larghezza è uguale all'impostazione della proprietà ScaleWidth del form.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Contenitore</p></td>
<td style="text-align: left;"><p>Sola lettura</p></td>
<td style="text-align: left;"><p>Restituisce il contenitore di un controllo in un form.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Abilitato</p></td>
<td style="text-align: left;"><p>Lettura/Scrittura</p></td>
<td style="text-align: left;"><p>Restituisce o imposta un valore che determina se un form o un controllo può rispondere agli eventi generati dall'utente.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Altezza</p></td>
<td style="text-align: left;"><p>Lettura/Scrittura</p></td>
<td style="text-align: left;"><p>Restituisce o imposta l'altezza di un oggetto.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>HWND</p></td>
<td style="text-align: left;"><p>Sola lettura</p></td>
<td style="text-align: left;"><p>Restituisce un handle per un form o un controllo.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Sinistra</p></td>
<td style="text-align: left;"><p>Lettura/Scrittura</p></td>
<td style="text-align: left;"><p>Restituisce o imposta la distanza tra il bordo interno sinistro di un oggetto e il bordo sinistro del relativo contenitore.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Nome</p></td>
<td style="text-align: left;"><p>Sola lettura</p></td>
<td style="text-align: left;"><p>Restituisce il nome utilizzato nel codice per identificare un form, un controllo o un oggetto di accesso ai dati.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Padre</p></td>
<td style="text-align: left;"><p>Sola lettura</p></td>
<td style="text-align: left;"><p>Restituisce il form, l'oggetto o la raccolta che contiene un controllo o un altro oggetto o raccolta.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>TabStop</p></td>
<td style="text-align: left;"><p>Lettura/Scrittura</p></td>
<td style="text-align: left;"><p>Restituisce o imposta un valore che indica se un utente può utilizzare il tasto <strong>Tab</strong> per assegnare lo stato attivo a un oggetto.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Inizio</p></td>
<td style="text-align: left;"><p>Lettura/Scrittura</p></td>
<td style="text-align: left;"><p>Restituisce o imposta la distanza tra il bordo superiore interno di un oggetto e il bordo superiore del relativo contenitore.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p>Visible</p></td>
<td style="text-align: left;"><p>Lettura/Scrittura</p></td>
<td style="text-align: left;"><p>Restituisce o imposta un valore che indica se un oggetto è visibile o nascosto.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p>Larghezza</p></td>
<td style="text-align: left;"><p>Lettura/Scrittura</p></td>
<td style="text-align: left;"><p>Restituisce o imposta la larghezza di un oggetto.</p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



 

 
