---
description: Identifica i possibili certificati del firmatario usati per firmare digitalmente le patch.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: Tabella MsiPatchCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39d2bc3a05c8b3fe3f23cd7dce01da36e14ce1f3984f24e827606bbc44c1a77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913311"
---
# <a name="msipatchcertificate-table"></a>Tabella MsiPatchCertificate

La tabella MsiPatchCertificate identifica i possibili certificati del firmatario usati per firmare digitalmente le patch. La tabella MsiPatchCertificate contiene le informazioni necessarie per abilitare l'applicazione di patch al controllo [dell'account](user-account-control--uac--patching.md) utente per un'applicazione.

La tabella MsiPatchCertificate include le colonne seguenti:



| Colonna               | Tipo                         | Chiave | Nullable |
|----------------------|------------------------------|-----|----------|
| PatchCertificate     | [Identificatore](identifier.md) | S   | N        |
| DigitalCertificate\_ | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate
</dt> <dd>

Identificatore univoco per questa riga nella tabella MsiPatchCertificate.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Chiave esterna nella prima colonna della [tabella MsiDigitalCertificate.](msidigitalcertificate-table.md) La riga indicata nella tabella MsiDigitalCertificate contiene la rappresentazione binaria del certificato del firmatario.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le patch vengono sempre valutate rispetto alla tabella MsiPatchCertificate corrente al momento dell'applicazione della patch. Una patch può modificare la tabella MsiPatchCertificate aggiungendo o rimuovendo voci. Ciò consente a una patch di modificare la valutazione delle patch future che verranno applicate più avanti nella sequenza di applicazione delle patch. Nella tabella possono essere presenti più certificati e la patch deve corrispondere ad almeno un certificato da applicare.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DisableLUAPatching](disableluapatching.md)
</dt> <dt>

[Applicazione di patch al controllo dell'account utente](user-account-control--uac--patching.md)
</dt> <dt>

[**MSIDISABLELUAPATCHING**](msidisableluapatching.md)
</dt> <dt>

[Firme digitali e programma di Windows di installazione](digital-signatures-and-windows-installer.md)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



