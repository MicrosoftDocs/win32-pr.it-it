---
description: Il metodo SourceListAddSource aggiunge un'origine di rete o URL. Accetta SourcePath, Type e Index come parametri. Questo metodo chiama MsiSourceListAddSourceEx.
ms.assetid: 61a8873f-c4ad-43d7-8bbb-5a2534ef2de7
title: Metodo Product.SourceListAddSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b95185cbd25354314eace5da7704da51dbbefe024ba8597c0eed41a688984117
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925871"
---
# <a name="productsourcelistaddsource-method"></a>Metodo Product.SourceListAddSource

Il **metodo SourceListAddSource** aggiunge un'origine di rete o URL. Accetta *SourcePath,**Type* e *Index* come parametri. Questo metodo chiama [**MsiSourceListAddSourceEx.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)

## <a name="syntax"></a>Sintassi


```JScript
Product.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tipo* 
</dt> <dd>

Tipo di origine da aggiungere: MSISOURCETYPE \_ NETWORK o MSISOURCETYPE \_ URL.

</dd> <dt>

*SourcePath* 
</dt> <dd>

Percorso dell'origine da aggiungere.

</dd> <dt>

*Index* 
</dt> <dd>

Se **SourceListAddSource viene chiamato** con una nuova origine e *Index* è impostato su 0, il programma di installazione aggiunge l'origine alla fine dell'elenco di origine.

Se questa funzione viene chiamata con un'origine già esistente nell'elenco di origine e *Index* è impostato su 0, il programma di installazione mantiene l'indice esistente dell'origine.

Se la funzione viene chiamata con un'origine esistente nell'elenco di origine e *Index* è impostato su un valore diverso da zero, l'origine viene rimossa dalla posizione corrente nell'elenco e inserita nella posizione specificata da *Index*, prima di qualsiasi origine già esistente in tale posizione.

Se la funzione viene chiamata con una nuova origine e *Index* è impostato su un valore diverso da zero, l'origine viene inserita nella posizione specificata da *Index*, prima di qualsiasi origine già esistente in tale posizione. Il valore di indice per tutte le origini nell'elenco dopo l'indice specificato da *Index* viene aggiornato per garantire che i valori di indice univoci e l'ordine preesistente rimanga invariato.

Se *Index* è maggiore del numero di origini nell'elenco, l'origine viene inserita alla fine dell'elenco con un valore di indice maggiore di uno rispetto a qualsiasi origine esistente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versione successiva in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto**](product-object.md)
</dt> <dt>

[**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




