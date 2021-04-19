---
description: Per un pacchetto di installazione, la proprietà riepilogo Numero revisione contiene il codice del pacchetto per il pacchetto di installazione.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Proprietà riepilogo Numero revisione
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e97df1eafec2d543be0f975b9f5daca7728267b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332316"
---
# <a name="revision-number-summary-property"></a>Proprietà riepilogo Numero revisione

Per un pacchetto di installazione, la proprietà **Riepilogo numero revisione** contiene il [*codice del pacchetto*](p-gly.md) per il pacchetto di installazione. Per ulteriori informazioni sui codici dei pacchetti, vedere [codici di pacchetto](package-codes.md).

Per una trasformazione, la proprietà **Riepilogo numero revisione** elenca i GUID del codice prodotto e la versione dei prodotti nuovi e originali e il GUID del codice di aggiornamento. L'elenco è separato da punti e virgola, come indicato di seguito.

"Originale-prodotto-codice originale-versione prodotto; New-Product codice nuovo-versione prodotto; Aggiornamento-codice "

Per un pacchetto di patch, la proprietà **Riepilogo numero revisione** specifica il codice della patch GUID per la patch. Questo può essere seguito da un elenco di GUID del codice patch per le patch obsolete che devono essere rimosse quando viene applicata questa patch. I codici patch sono concatenati senza delimitatori che separano i GUID nell'elenco.

* * Windows Installer 3,0: * * se nella [tabella MsiPatchSequence](msipatchsequence-table.md)sono presenti informazioni di sequenziazione, Windows Installer 3,0 usa le informazioni di sequenziazione nella tabella e ignora l'elenco delle patch obsolete incluse nella proprietà di **Riepilogo dei numeri di revisione** . Windows Installer 3,0 può comunque utilizzare le informazioni sulla patch obsolete nella proprietà **Riepilogo numero revisione** se il pacchetto non contiene una tabella MsiPatchSequence.

* * Windows Installer 2,0: * * la [tabella MsiPatchSequence](msipatchsequence-table.md) non è supportata. Windows Installer 2,0 può comunque utilizzare le informazioni sulla patch obsolete nella proprietà **Riepilogo numero revisione** se il pacchetto non contiene una tabella MsiPatchSequence.

Questa proprietà di riepilogo è obbligatoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




