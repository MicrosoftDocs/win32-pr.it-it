---
description: Il metodo SourceListAddSource aggiunge un'origine di rete o URL. Accetta SourcePath, Type e index come parametri. Questo metodo chiama MsiSourceListAddSourceEx.
ms.assetid: 61a8873f-c4ad-43d7-8bbb-5a2534ef2de7
title: Metodo Product. SourceListAddSource
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
ms.openlocfilehash: e0cfda9b8eab0e7dd00afd15eb701a6e7decf2ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326537"
---
# <a name="productsourcelistaddsource-method"></a>Metodo Product. SourceListAddSource

Il metodo **SourceListAddSource** aggiunge un'origine di rete o URL. Accetta *SourcePath*,*Type* e *index* come parametri. Questo metodo chiama [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).

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

Tipo di origine da aggiungere: MSISOURCETYPE \_ Network o MSISOURCETYPE \_ URL.

</dd> <dt>

*SourcePath* 
</dt> <dd>

Percorso dell'origine da aggiungere.

</dd> <dt>

*Index* 
</dt> <dd>

Se **SourceListAddSource** viene chiamato con una nuova origine e *index* è impostato su 0, il programma di installazione aggiunge l'origine alla fine dell'elenco di origine.

Se questa funzione viene chiamata con un'origine già esistente nell'elenco di origine e *index* è impostato su 0, il programma di installazione mantiene l'indice esistente dell'origine.

Se la funzione viene chiamata con un'origine esistente nell'elenco di origine e *index* è impostato su un valore diverso da zero, l'origine viene rimossa dalla posizione corrente nell'elenco e inserita in corrispondenza della posizione specificata da *index*, prima di qualsiasi origine già esistente in tale posizione.

Se la funzione viene chiamata con una nuova origine e *index* è impostato su un valore diverso da zero, l'origine viene inserita in corrispondenza della posizione specificata da *index*, prima di qualsiasi origine già presente in tale posizione. Il valore di indice per tutte le origini nell'elenco dopo l'indice specificato dall' *Indice* viene aggiornato per garantire che i valori di indice univoci e l'ordine preesistente rimangano invariati.

Se l' *Indice* è maggiore del numero di origini nell'elenco, l'origine viene posizionata alla fine dell'elenco con un valore di indice maggiore di quello di un'origine esistente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct è definito come 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Prodotto**](product-object.md)
</dt> <dt>

[**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




