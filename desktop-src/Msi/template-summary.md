---
description: Per un pacchetto di installazione, la proprietà Riepilogo modello indica le versioni della piattaforma e della lingua compatibili con questo database di installazione.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Proprietà Riepilogo modello
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da93d2d3a38f3c1853f3f936fe6f97b8550dcaeac70d4b553b8cb0362f41ee41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893451"
---
# <a name="template-summary-property"></a>Proprietà Riepilogo modello

Per un pacchetto di installazione, la **proprietà Riepilogo** modello indica le versioni della piattaforma e della lingua compatibili con questo database di installazione. La sintassi delle **informazioni sulle proprietà riepilogo** modello per un database di installazione è la seguente:

\[*proprietà della piattaforma* \] ; \[ *language id* \] \[ , language id *,...* \] \[ \] .

Gli esempi seguenti sono valori validi per la **proprietà Riepilogo** modello:

-   x64;1033
-   Intel;1033
-   Intel64;1033
-   ;1033
-   Intel ;1033,2046
-   Intel64;1033,2046
-   Intel;0
-   Arm;1033,2046
-   Arm;0
-   Arm64;1033,2046
-   Arm64;0

La **proprietà Riepilogo** modello di una trasformazione indica la piattaforma e le versioni del linguaggio compatibili con la trasformazione. In un file di trasformazione può essere specificata una sola lingua. La piattaforma e il linguaggio specificati determinano se una trasformazione può essere applicata a un database specifico. La proprietà della piattaforma e la proprietà language possono essere lasciati vuoti se nessuna restrizione di trasformazione si basa su di esse per convalidare la trasformazione.

La **proprietà Riepilogo** modello di un pacchetto patch è un elenco delimitato da punto e virgola dei codici prodotto che possono accettare la patch. Se si usano [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) per generare il pacchetto di patch, questo elenco viene ottenuto dalla tabella [TargetImages](targetimages-table-patchwiz-dll-.md) del file di creazione della patch.

Questa proprietà di riepilogo è obbligatoria.

## <a name="remarks"></a>Commenti

Se la piattaforma corrente non corrisponde a una delle piattaforme specificate nella proprietà **Riepilogo** modello, il programma di installazione non elabora il pacchetto.

Se la specifica della piattaforma non è presente nel **valore della proprietà Riepilogo** modello, il programma di installazione presuppone l'architettura Intel.

Se si tratta di un pacchetto Windows Installer a 64 bit in esecuzione in una piattaforma Intel64 (Itanium), immettere Intel64 nella proprietà **Riepilogo** modello.

Se si tratta di un pacchetto Windows installer a 64 bit in esecuzione in una piattaforma x64, immettere x64 nella **proprietà Riepilogo** modello.

Se si tratta di un pacchetto Windows Installer a 64 bit in esecuzione in una piattaforma Arm64, immettere Arm64 nella proprietà **Riepilogo** modello.

Un Windows installer non può essere contrassegnato come che supporta sia Intel64 che x64; Ad esempio, il **valore della proprietà Riepilogo** modello di Intel64,x64 non è valido.

Un Windows installer non può essere contrassegnato come che supporta piattaforme a 32 bit e a 64 bit. Ad esempio, **i valori delle** proprietà riepilogo modello, ad esempio Intel,x64 o Intel,Intel64 non sono validi.

Se si immette 0 (zero) nel campo language ID (ID lingua) della proprietà **Template Summary** (Riepilogo modello) o si lascia vuoto questo campo, indica che il pacchetto è indipendente dalla lingua.

Se si tratta di un Windows installer in esecuzione Windows RT, immettere il valore Arm nella **proprietà Riepilogo** modello.

I moduli unione sono gli unici pacchetti che possono avere più lingue. In un database del programma di installazione di origine è possibile specificare una sola lingua. Per altre informazioni, vedere [Multiple Language Merge Modules](multiple-language-merge-modules.md).

La piattaforma Alpha non è supportata dal programma Windows di installazione.

**Windows programma di installazione:** La sintassi seguente non è supportata:

\[*platform property* \] \[ , platform *property* \] \[ ,... \] \[ *language id* \] \[ , language id *,...* \] \[ \] .

Gli esempi seguenti non sono valori validi per la **proprietà Riepilogo** modello:

-   Alpha,Intel;1033
-   Intel,Alpha;1033
-   Alfa;1033
-   Alpha;1033,2046

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




