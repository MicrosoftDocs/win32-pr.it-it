---
description: Il metodo AdvertiseProduct dell'oggetto Installer annuncia un pacchetto di installazione.
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: Metodo Installer::AdvertiseProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a3792b279df9ac43fc09eaa02005cdaf3373e341bf2df40ce0a350d6c31bd47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633290"
---
# <a name="installeradvertiseproduct-method"></a>Metodo Installer::AdvertiseProduct

Il **metodo AdvertiseProduct** dell'oggetto [**Installer**](installer-object.md) annuncia un pacchetto di installazione.

## <a name="syntax"></a>Sintassi


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*packagePath* 
</dt> <dd>

Percorso completo del pacchetto Windows Installer (.msi) da annunciare.

</dd> <dt>

*context* 
</dt> <dd>

Contesto dell'annuncio. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt> </dl> | Annuncia l'applicazione per un'istanza nel contesto di installazione per [computer.](installation-context.md) In questo modo il pacchetto è disponibile per l'installazione da parte di tutti gli utenti del computer.<br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <dt>**msiAdvertiseProductUser**</dt> <dt>1</dt> </dl>             | Annuncia l'applicazione per un'installazione nel contesto di installazione per [utente](installation-context.md).<br/>                                                                                   |



 

</dd> <dt>

*Trasforma* 
</dt> <dd>

Elenco di trasformazioni da applicare al prodotto. Le trasformazioni nell'elenco sono delimitate da punti e virgola. Questo parametro è facoltativo.

</dd> <dt>

*language* 
</dt> <dd>

Lingua del pacchetto di installazione da utilizzare. Questo parametro è facoltativo.

</dd> <dt>

*options* 
</dt> <dd>

Opzioni dell'annuncio. Questo parametro è facoltativo. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**msiAdvertiseDefault**</dt> <dt>0</dt> </dl>                             | Annuncio standard<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt> </dl> | Annuncia una nuova istanza del prodotto. Richiede che la prima trasformazione nell'elenco delle trasformazioni del parametro *transforms* sia la trasformazione dell'istanza che modifica il codice del prodotto. Per altre informazioni, vedere [Installazione di più istanze di prodotti e patch.](installing-multiple-instances-of-products-and-patches.md)<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il **metodo AdvertiseProduct** usa la [**funzione MsiAdvertiseProductEx.**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)

## <a name="examples"></a>Esempio

L'esempio seguente illustra l'uso del **metodo AdvertiseProduct.**


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 4.5 in Windows Server 2003 e Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Programma di installazione**](installer-object.md)
</dt> <dt>

[Non supportato in Windows Installer 3.1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




