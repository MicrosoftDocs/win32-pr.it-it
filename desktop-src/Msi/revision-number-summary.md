---
description: Per un pacchetto di installazione, la proprietà Riepilogo numero revisione contiene il codice del pacchetto del programma di installazione.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Proprietà Riepilogo numero revisione
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11371c4a431322fd7ceca7fd645fc8eb8bea47688b740340e973507271f6a25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869061"
---
# <a name="revision-number-summary-property"></a>Proprietà Riepilogo numero revisione

Per un pacchetto di installazione, la **proprietà Riepilogo numero** revisione contiene il codice del [*pacchetto*](p-gly.md) del programma di installazione. Per altre informazioni sui codici pacchetto, vedere [Codici pacchetto](package-codes.md).

Per una trasformazione, la **proprietà Riepilogo numero** revisione elenca i GUID del codice prodotto e la versione dei prodotti nuovi e originali e il GUID del codice di aggiornamento. L'elenco è separato da punti e virgola come indicato di seguito.

"Original-Product-Code Original-Product-Version ; New-Product Code New-Product-Version; Upgrade-Code"

Per un pacchetto patch, la **proprietà Revision Number Summary** specifica il codice di patch GUID per la patch. Questo può essere seguito da un elenco di GUID del codice patch per le patch obsolete che devono essere rimosse quando viene applicata questa patch. I codici patch vengono concatenati senza delimitatori che separano i GUID nell'elenco.

**Windows Installer 3.0: ** Se sono presenti informazioni di sequenziazione nella tabella [MsiPatchSequence](msipatchsequence-table.md), Windows Installer 3.0 usa le informazioni di sequenziazione nella tabella e ignora l'elenco di patch obsolete incluse nella proprietà **Revision Number Summary.** Windows Il programma di installazione 3.0 può comunque usare le informazioni sulla patch obsolete nella proprietà **Riepilogo** numero revisione se il pacchetto non contiene una tabella MsiPatchSequence.

**Windows Installer 2.0: ** La tabella [MsiPatchSequence](msipatchsequence-table.md) non è supportata. Windows Il programma di installazione 2.0 può comunque usare le informazioni sulla patch obsolete nella proprietà **Riepilogo** numero revisione se il pacchetto non contiene una tabella MsiPatchSequence.

Questa proprietà di riepilogo è obbligatoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




