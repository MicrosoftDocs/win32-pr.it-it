---
description: Il metodo DVDAdm. ChangePassword salva una nuova password dell'applicazione nel registro di sistema.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: ChangePassword (metodo)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba8bfb9adcecdb88f19f3ac1b8061f93486e269
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481029"
---
# <a name="changepassword-method"></a>ChangePassword (metodo)

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `DVDAdm.ChangePassword` metodo salva una nuova password dell'applicazione nel registro di sistema.

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Specifica il nome di accesso dell'utente corrente sotto forma di stringa. Il parametro viene ignorato dall'oggetto MSDVDAdm. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*Venduti*
</dt> <dd>

Specifica la vecchia password dell'utente sotto forma di stringa.

</dd> <dt>

<span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*
</dt> <dd>

Specifica la nuova password dell'utente sotto forma di stringa. Non può essere una stringa vuota.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Attualmente, il parametro *sUserName* viene ignorato in questo e in tutti i metodi correlati. Ciò significa che chiunque conosca la password può impostare il livello padre. Sono disponibili solo una password e un livello parentale per l'applicazione. Non è disponibile alcun supporto per i nomi di accesso utente singoli o per la gestione di più password. Per applicare i livelli di gestione padre, i genitori devono impostare la password e quindi impostare il livello padre appropriato per i membri più giovani del gruppo di parenti. Quando i genitori vogliono visualizzare un disco con contenuto con classificazione adulta, possono modificare il livello e quindi modificarlo di nuovo al termine della visualizzazione. Finché gli elementi figlio non conoscono la password, possono solo controllare il contenuto al di sotto del livello impostato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ConfirmPassword**](confirmpassword-method.md)
</dt> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



