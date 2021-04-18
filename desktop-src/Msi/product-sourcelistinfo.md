---
description: La proprietà SourceListInfo dell'oggetto Product ottiene e imposta le proprietà delle informazioni di origine per un prodotto. Questa proprietà chiama MsiSourceListGetInfo o MsiSourceListSetInfo. Si tratta di una proprietà di lettura o scrittura.
ms.assetid: 3a2c4af5-592f-4acd-b7d8-df163e00b1e2
title: Proprietà Product. SourceListInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 23fff0cd478a8345e72b79632817e856c40eb7b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330624"
---
# <a name="productsourcelistinfo-property"></a>Proprietà Product. SourceListInfo

La proprietà **SourceListInfo** dell'oggetto [**Product**](product-object.md) ottiene e imposta le proprietà delle informazioni di origine per un prodotto. Questa proprietà chiama [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) o [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa). Si tratta di una proprietà di lettura o scrittura.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Product.SourceListInfo
```



## <a name="property-value"></a>Valore proprietà

Nome delle proprietà delle informazioni di origine per un prodotto da interrogare o impostare. Per i valori possibili, vedere la sezione Osservazioni di questo argomento.

## <a name="remarks"></a>Commenti

Non è possibile impostare tutte le proprietà che possono essere recuperate. Il parametro *szProperty* può essere uno dei valori seguenti.



| Proprietà         | È possibile impostare? | Significato                                                                                                                                                                                                                                                        |
|------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MediaPackagePath | S        | Percorso relativo alla radice del supporto di installazione.                                                                                                                                                                                                       |
| DiskPrompt       | S        | Modello di richiesta utilizzato quando viene richiesto all'utente il supporto di installazione.                                                                                                                                                                                       |
| LastUsedSource   | S        | Il percorso di origine utilizzato più di recente per il prodotto. Quando si imposta questa proprietà, anteporre il prefisso "n;" al percorso di origine di rete o "u;" per il tipo di URL. Ad esempio, "n; \\ \\ Scratch \\ My \\ source "e" u; https://MyServer/MyFolder/MySource ". |
| LastUsedType     | N        | "n" se l'ultima origine usata è un percorso di rete. "u" se l'ultima origine usata era un percorso URL. "m" se l'ultima origine usata era un supporto. Stringa vuota ("") se non è disponibile l'ultima origine usata.                                                                   |
| PackageName      | S        | Nome del pacchetto di Windows Installer o del pacchetto di patch nell'origine.                                                                                                                                                                                      |



 

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

[**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




