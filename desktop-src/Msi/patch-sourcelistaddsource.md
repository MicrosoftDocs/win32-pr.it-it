---
description: Il metodo SourceListAddSource aggiunge un'origine di rete o URL. Accetta SourcePath, Type e Index come parametri. Questo metodo chiama MsiSourceListAddSourceEx.
ms.assetid: 87797a8c-f1ba-4bfb-9296-3d3ef2a3c37f
title: Metodo Patch.SourceListAddSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 712551a31868ad3a97738ce9f49c9b0ff3526cf33cbae0ca5dd284f701869666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519601"
---
# <a name="patchsourcelistaddsource-method"></a>Metodo Patch.SourceListAddSource

Il **metodo SourceListAddSource** aggiunge un'origine di rete o URL. Accetta *SourcePath*, *Type e* *Index* come parametri. Questo metodo chiama [**MsiSourceListAddSourceEx.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)

## <a name="syntax"></a>Sintassi


```JScript
Patch.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tipo* 
</dt> <dd>

Tipo di origine da aggiungere: MSISOURCETYPE \_ NETWORK o URL MSISOURCETYPE. \_

</dd> <dt>

*SourcePath* 
</dt> <dd>

Percorso dell'origine da aggiungere.

</dd> <dt>

*Index* 
</dt> <dd>

Se **SourceListAddSource viene chiamato** con una nuova origine e *Index* impostato su 0, il programma di installazione aggiunge l'origine alla fine dell'elenco di origine.

Se questa funzione viene chiamata con un'origine già esistente nell'elenco di origine e *Index* è impostato su 0, il programma di installazione mantiene l'indice esistente dell'origine.

Se la funzione viene chiamata con un'origine esistente nell'elenco di origine e *Index* è impostato su un valore diverso da zero, l'origine viene rimossa dalla posizione corrente nell'elenco e inserita nella posizione specificata da *Index*, prima di qualsiasi origine già esistente in tale posizione.

Se la funzione viene chiamata con una nuova origine e *Index* è impostato su un valore diverso da zero, l'origine viene inserita nella posizione specificata da *Index*, prima di qualsiasi origine già esistente in tale posizione. Il valore di indice per tutte le origini nell'elenco dopo l'indice specificato da *Index* viene aggiornato per garantire che i valori di indice univoci e l'ordine preesistente rimanga invariato.

Se *Index* è maggiore del numero di origini nell'elenco, l'origine viene posizionata alla fine dell'elenco con un valore di indice maggiore di uno rispetto a qualsiasi origine esistente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IPatch IID è definito come \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




