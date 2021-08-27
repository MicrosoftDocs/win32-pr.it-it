---
description: L'interfaccia IExtender fornisce un set di proprietà di base che vengono aggiunte all'interfaccia di un controllo . I programmatori possono usare queste proprietà come se fossero parte del controllo.
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
ms.openlocfilehash: a341f5d8a0ec554f008232f44156486df83d0fd8
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625114"
---
# <a name="iextender-interface"></a>Interfaccia IExtender

**L'interfaccia IExtender** fornisce un set di proprietà di base che vengono aggiunte all'interfaccia di un controllo . I programmatori possono usare queste proprietà come se fossero parte del controllo.

## <a name="members"></a>Membri

**L'interfaccia IExtender** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IExtender** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IExtender** include questi metodi.



| Metodo                         | Descrizione                                    |
|:-------------------------------|:-----------------------------------------------|
| [**Sposta**](iextender-move.md) | Sposta un oggetto MDIForm, un form o un controllo.<br/> |



 

### <a name="properties"></a>Proprietà

**L'interfaccia IExtender** ha queste proprietà.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Proprietà</th>
<th >Tipo di accesso</th>
<th >Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td >Allinea<br/></td>
<td >Lettura/Scrittura<br/></td>
<td >Restituisce o imposta un valore che determina se un oggetto viene visualizzato con qualsiasi dimensione in un punto qualsiasi di un form o se viene visualizzato nella parte superiore, inferiore, sinistra o destra del form e viene ridimensionato automaticamente in base alla larghezza del form.<br/> 
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
<td>(impostazione predefinita in un form non MDI) Nessuno: le dimensioni e la posizione possono essere impostate in fase di progettazione o nel codice. L'impostazione viene ignorata se l'oggetto si trova in un form MDI.</td>
</tr>
<tr class="even">
<td>vbAlignTop 1</td>
<td>(impostazione predefinita in un form MDI) Top: l'oggetto si trova nella parte superiore del form e la larghezza è uguale all'impostazione della proprietà ScaleWidth del form.</td>
</tr>
<tr class="odd">
<td>vbAlignBottom 2</td>
<td>Bottom: l'oggetto si trova nella parte inferiore del form e la larghezza è uguale all'impostazione della proprietà ScaleWidth del form.</td>
</tr>
<tr class="even">
<td>vbAlignLeft 3</td>
<td>Left: l'oggetto si trova a sinistra del form e la larghezza è uguale all'impostazione della proprietà ScaleWidth del form.</td>
</tr>
<tr class="odd">
<td>vbAlignRight 4</td>
<td>Right: l'oggetto si trova a destra del form e la larghezza è uguale all'impostazione della proprietà ScaleWidth del form.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><p>Contenitore</p></td>
<td ><p>Sola lettura</p></td>
<td ><p>Restituisce il contenitore di un controllo in un form.</p></td>
</tr>
<tr class="odd">
<td ><p>Attivato</p></td>
<td ><p>Lettura/Scrittura</p></td>
<td ><p>Restituisce o imposta un valore che determina se un form o un controllo può rispondere agli eventi generati dall'utente.</p></td>
</tr>
<tr class="even">
<td ><p>Altezza</p></td>
<td ><p>Lettura/Scrittura</p></td>
<td ><p>Restituisce o imposta l'altezza di un oggetto .</p></td>
</tr>
<tr class="odd">
<td ><p>Hwnd</p></td>
<td ><p>Sola lettura</p></td>
<td ><p>Restituisce un handle a un form o a un controllo.</p></td>
</tr>
<tr class="even">
<td ><p>Sinistra</p></td>
<td ><p>Lettura/Scrittura</p></td>
<td ><p>Restituisce o imposta la distanza tra il bordo sinistro interno di un oggetto e il bordo sinistro del relativo contenitore.</p></td>
</tr>
<tr class="odd">
<td ><p>Nome</p></td>
<td ><p>Sola lettura</p></td>
<td ><p>Restituisce il nome utilizzato nel codice per identificare un form, un controllo o un oggetto di accesso ai dati.</p></td>
</tr>
<tr class="even">
<td ><p>Padre</p></td>
<td ><p>Sola lettura</p></td>
<td ><p>Restituisce il form, l'oggetto o la raccolta che contiene un controllo o un altro oggetto o raccolta.</p></td>
</tr>
<tr class="odd">
<td ><p>Tabstop</p></td>
<td ><p>Lettura/Scrittura</p></td>
<td ><p>Restituisce o imposta un valore che indica se un utente può utilizzare il tasto <strong>TAB</strong> per assegnare lo stato attivo a un oggetto .</p></td>
</tr>
<tr class="even">
<td ><p>Inizio</p></td>
<td ><p>Lettura/Scrittura</p></td>
<td ><p>Restituisce o imposta la distanza tra il bordo superiore interno di un oggetto e il bordo superiore del relativo contenitore.</p></td>
</tr>
<tr class="odd">
<td ><p>Visible</p></td>
<td ><p>Lettura/Scrittura</p></td>
<td ><p>Restituisce o imposta un valore che indica se un oggetto è visibile o nascosto.</p></td>
</tr>
<tr class="even">
<td ><p>Larghezza</p></td>
<td ><p>Lettura/Scrittura</p></td>
<td ><p>Restituisce o imposta la larghezza di un oggetto .</p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



 

 
