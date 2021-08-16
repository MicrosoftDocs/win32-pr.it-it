---
description: Ottiene l'oggetto ISearchItem se l'URL rappresenta un'origine dati Shell effettiva (nota anche come estensione dello spazio dei nomi Shell).
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: Metodo ISearchItem::GetParentFolder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem.GetParentFolder
api_type:
- COM
api_location: ''
ms.openlocfilehash: a5e5aded87ca197af8774a7b5506e21c958dc564eb0af67396e100877ac53e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094911"
---
# <a name="isearchitemgetparentfolder-method"></a>Metodo ISearchItem::GetParentFolder

Ottiene [**l'oggetto ISearchItem**](-search-isearchitem.md) se l'URL rappresenta un'origine dati Shell effettiva (nota anche come estensione dello spazio dei nomi Shell).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IShellFolder* \[ Cambio\]
</dt> <dd>

Tipo: **ppShellFolder \* \***

In caso di restituzione, contiene l'indirizzo di un puntatore alla cartella che contiene l'URL corrente. [L'interfaccia IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) viene esposta da tutti gli oggetti cartella dello spazio dei nomi shell e i relativi metodi vengono usati per gestire le cartelle.

</dd> <dt>

*LPITEMIDLIST* \[ Cambio\]
</dt> <dd>

Tipo: **ppidl \***

In caso di restituzione, contiene l'indirizzo di un puntatore a un elenco di identificatori di elemento (PIDL) che identifica la cartella padre. Il *parametro LPITEMIDLIST* può fare riferimento a un oggetto a qualsiasi livello al di sotto della cartella padre nella gerarchia dello spazio dei nomi e può quindi essere un puntatore a più livelli a un **pidl** relativo alla cartella padre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il **metodo ISearchItem::GetParentFolder** è supportato solo in Windows XP e Windows Server 2003 e non deve più essere usato.

Per visualizzare in anteprima gli allegati con un gestore di protocollo di terze parti nei computer che eseguono Windows XP o Windows Server 2003, potrebbe essere necessario usare l'interfaccia [**ISearchItem**](-search-isearchitem.md) e le API seguenti: le interfacce [**IItemPreviewerExt,**](-search-iitempreviewerext.md) [**IItemPropertyBag**](iitempropertybag.md)e [**ISearchProtocolUI,**](-search-isearchprotocolui.md) la struttura [**LINKINFO**](-search-linkinfo.md) e l'enumerazione [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISearchItem**](-search-isearchitem.md)
</dt> </dl>

 

 
