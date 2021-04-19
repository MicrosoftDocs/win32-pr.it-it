---
description: Per un pacchetto di installazione, la proprietà di riepilogo del modello indica le versioni della piattaforma e della lingua compatibili con il database di installazione.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Proprietà di riepilogo del modello
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b3949e7028fd0b1b5f9ff3112f1a3d03c9b87e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326368"
---
# <a name="template-summary-property"></a>Proprietà di riepilogo del modello

Per un pacchetto di installazione, la proprietà di **Riepilogo del modello** indica le versioni della piattaforma e della lingua compatibili con il database di installazione. La sintassi delle informazioni sulle proprietà di **Riepilogo dei modelli** per un database di installazione è la seguente:

\[*Proprietà Platform* \] ; \[ *ID lingua* \] \[ ,*ID lingua* \] \[ ,... \] .

Gli esempi seguenti sono valori validi per la proprietà di **Riepilogo del modello** :

-   x64; 1033
-   Intel; 1033
-   Intel64; 1033
-   ; 1033
-   Intel; 1033, 2046
-   Intel64; 1033, 2046
-   Intel; 0
-   ARM; 1033, 2046
-   ARM; 0
-   Arm64; 1033, 2046
-   Arm64; 0

La proprietà di **Riepilogo del modello** di una trasformazione indica le versioni della piattaforma e della lingua compatibili con la trasformazione. In un file di trasformazione è possibile specificare solo una lingua. La piattaforma e la lingua specificate determinano se una trasformazione può essere applicata a un determinato database. La proprietà Platform e la proprietà Language possono essere lasciate vuote se nessuna restrizione di trasformazione si basa su di esse per convalidare la trasformazione.

La proprietà di **Riepilogo dei modelli** di un pacchetto di patch è un elenco delimitato da punti e virgola dei codici prodotto che possono accettare la patch. Se si usa [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) per generare il pacchetto di patch, questo elenco viene ottenuto dalla [tabella TargetImages](targetimages-table-patchwiz-dll-.md) del file di creazione della patch.

Questa proprietà di riepilogo è obbligatoria.

## <a name="remarks"></a>Commenti

Se la piattaforma corrente non corrisponde a una delle piattaforme specificate nella proprietà di **Riepilogo del modello** , il programma di installazione non elabora il pacchetto.

Se la specifica della piattaforma non è presente nel valore della proprietà di **Riepilogo del modello** , il programma di installazione presuppone l'architettura Intel.

Se si tratta di un pacchetto Windows Installer a 64 bit in esecuzione su una piattaforma Intel64 (Itanium), immettere Intel64 nella proprietà di **Riepilogo del modello** .

Se si tratta di un pacchetto Windows Installer a 64 bit eseguito su una piattaforma x64, immettere x64 nella proprietà di **Riepilogo del modello** .

Se si tratta di un pacchetto Windows Installer a 64 bit in esecuzione su una piattaforma Arm64, immettere Arm64 nella proprietà di **Riepilogo del modello** .

Non è possibile contrassegnare un pacchetto di Windows Installer come supporto sia per Intel64 che per x64; ad esempio, il valore della proprietà di **Riepilogo del modello** di Intel64, x64 non è valido.

Non è possibile contrassegnare un pacchetto di Windows Installer come supporto per piattaforme a 32 bit e a 64 bit. ad esempio, i valori delle proprietà di **Riepilogo dei modelli** come Intel, x64 o Intel, Intel64 non sono validi.

Se si immette 0 (zero) nel campo ID lingua della proprietà **Riepilogo modello** o si lascia vuoto questo campo, viene indicato che il pacchetto è indipendente dalla lingua.

Se si tratta di un pacchetto Windows Installer in esecuzione in Windows RT, immettere il valore ARM nella proprietà di **Riepilogo del modello** .

I moduli merge sono gli unici pacchetti che possono avere più lingue. In un database del programma di installazione di origine è possibile specificare solo una lingua. Per ulteriori informazioni, vedere la pagina relativa ai [moduli merge con più lingue](multiple-language-merge-modules.md).

La piattaforma Alpha non è supportata da Windows Installer.

**Windows Installer:** La sintassi seguente non è supportata:

\[*Proprietà Platform* \] \[ ,*Proprietà Platform* \] \[ \] ,... \[ *ID lingua* \] \[ ,*ID lingua* \] \[ ,... \] .

Gli esempi seguenti non sono valori validi per la proprietà di **Riepilogo dei modelli** :

-   Alfa, Intel; 1033
-   Intel, Alpha; 1033
-   Alfa; 1033
-   Alfa; 1033, 2046

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




